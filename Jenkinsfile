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
    
       cron('H H(9-16)/2 * * 1-5')
    
     }
   
      stages  {
      stage ('Build'){
        steps {
           
            sh '''
            sleep 10
            echo  $Chandan_s
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




