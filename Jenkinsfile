pipeline {
     agent any
     
     Stages{  stage('DeployToProduction') {
             steps {

            
             kubernetesDeploy(

                    kubeconfigId: 'kubeconfiguration',

                    configs: 'deploymentfile.yml',

                    enableConfigSubstitution: true   
             )

            }

             
             }
     
           }
     
}





    



