pipeline {
     agent any
     
     stages{  
          stage('DeployToProduction') {
             steps {

            
             kubernetesDeploy(

                    kubeconfigId: 'kubeconfig',

                    configs: 'deploymentfile.yml',

                    enableConfigSubstitution: true   
             )

            }

             
             }
     
           }
     

}





    



