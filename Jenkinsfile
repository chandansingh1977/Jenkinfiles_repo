pipeline {
    agent any
environment {
    TEST = "test_value"
}
parameters {name: 'Chandan_s' , defaultValue: 'input_chandan' , description: 'this is a string parameter'

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




