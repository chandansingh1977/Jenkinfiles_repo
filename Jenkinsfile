pipeline {
    agent any
   
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
                 sleep 10
                  '''
          }
      } 
        stage ('Test'){
          steps {
             catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
              sh '''
              sleep 10
              exit 1
           }       '''
        }
    }
      stage ('Deploy'){
        steps {
             sh '''
             sleep 10
             '''
          }
      }  
 }

}


}