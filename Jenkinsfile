pipeline {
    agent any
environment {
    TEST = "test_value"
    TEST1 = "test_value1"
}
    stages  {
    stage ('Build'){
        steps {
           
            sh '''
            sleep 10
            echo $TEST $TEST1
            '''
    }
        
}
    stage ('Test'){
        steps {
          sh '''
            #!/bin/bash
            echo $TEST $TEST1
            sleep 5
            '''
        }


   }


 }



}




