pipeline {
    agent any
    environment {
    TEST = "test_value"
}
    parameters {
     string(name: 'Chandan_s' , defaultValue: 'input_chandan' , description: 'this is a string parameter')
     booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
 }
     triggers{ 
    
       cron('*/59 * * * *')
    
     }
   
      stages  {
         stage ('Checkout'){
          steps {
           checkout([$class: 'GitSCM',
           branches: [[name: '*/main']],
           userRemoteConfigs: [[url: 'https://github.com/chandansingh1977/First_repository.git',
           credintialsID: 'github' ]]])
          }      
    }
  
  
             stage ('Build') {
             steps {
                 sh '''
                 ls -lrt
                  '''
          }
      }      
        stage ('Test'){
        steps {
          script {
              echo "${params.Chandan_s}"
          }
      }  
        }
 }

}




