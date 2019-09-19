pipeline {
     stage('SCM') {
            steps {
                git url: 'https://github.com/MishraKD/firstJava.git'
            }
        }
    stage('codeQuality & analysis') {
        steps {
                withSonarQubeEnv('My SonarQube Server') {
                    // Optionally use a Maven environment you've configured already
                    withMaven(maven:'Maven 3.0.4') {
                        sh 'mvn clean package sonar:sonar'
                    }
                }
            }
    }
     stage('Security Yasca') {
    }
     stage('kubernetesDeployment') {
    }
    
     stage('regression') {
    }
     stage('perfomance') {
    }
}
   /* agent any

    environment {

        //Input Docker registry name and image name

        DOCKER_IMAGE_NAME = "deepk/assign2:1.2"

    }
    
   
   
    stages {
         
        stage('pull docker images') {
            agent {
                docker { image 'deepk/assign2:1.2' }
            }
        }

        stage('Build Docker Image') {

            when {

                branch 'master'

            }

            steps {

                script {

                    app = docker.build(DOCKER_IMAGE_NAME)

                    //app.inside {

                       sh 'echo Hello, World!'

                    //}

                }

            }

        }

        //perform Docker push

        stage('Push Docker Image') {

            when {

                branch 'master'

            }

            steps {

                script {

                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub_login') {

                        app.push("${env.BUILD_NUMBER}")

                        app.push("latest")

                    }

                }

                

            }

        }

        stage('DeployToProduction') {

            when {

                branch 'master'

            }

            steps {

                //input 'Deploy to Production?'

                //milestone(1)

                kubernetesDeploy(

                    kubeconfigId: 'kubeconfig',

                    configs: 'deploymentfile.yml',

                    enableConfigSubstitution: true

                )

            }

        }

    }
    */



