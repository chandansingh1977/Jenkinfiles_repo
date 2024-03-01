pipeline {
      agent any

parameters {
 booleanParam(name: 'CHECKOUT', defaultValue: true, description: 'Toggle this value') 
 booleanParam(name: 'BUILD', defaultValue: true, description: 'Toggle this value') 
 booleanParam(name: 'TEST', defaultValue: true, description: 'Toggle this value') 
 booleanParam(name: 'DEPLOY', defaultValue: false, description: 'Toggle this value') 

 }
  
      stages  {
         stage ('Checkout'){
         when {
          expression {
            params.CHECKOUT == true
          }

         }
         
          steps {
           checkout([$class: 'GitSCM',
           branches: [[name: '*/main']],
           userRemoteConfigs: [[url: 'https://github.com/chandansingh1977/First_repository.git',
           credintialsID: 'github' ]]])
          }      
    }

               stage ('Build') {
             when {
          expression {
            params.BUILD == true
          }

         }
           
             steps {
                 sh '''
                 sleep 10
                  '''
          }
      } 
        stage ('Test') {
          when {
          expression {
            params.TEST == true
          }

         }
          steps {
             catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
              sh '''
              sleep 10
              exit 1
                 '''
           } 
        }
    }
      stage ('Deploy'){
        when {
          expression {
            params.DEPLOY == true
          }

         }
        steps {
             sh '''
             sleep 10
             '''
          }
      }  
 }

}     

