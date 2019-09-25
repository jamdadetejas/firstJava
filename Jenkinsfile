pipeline {
     agent any
     
             stage('DeployToProduction') {
             steps {

            
             kubernetesDeploy(

                    kubeconfigId: 'kubeconfiguration',

                    configs: 'deploymentfile.yml',

                    enableConfigSubstitution: true   
             )

            }

             
             }
     
     
     
}





    



