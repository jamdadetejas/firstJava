pipeline {
     agent any
     
     stages{  
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
     

}





    



