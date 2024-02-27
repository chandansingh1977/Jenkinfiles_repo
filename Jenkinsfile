pipeline {
    agent none
environment {
    TEST = "test_value"
    TEST1 = "test_value1"
}
    stages  {
    stage ('Build'){
         agent {
        label 'install_jenkin'
    }
        steps {
            sh 
            '''
            sleep 10
            echo $TEST $TEST1
            '''
    }
        
}
    stage ('Test'){
        agent any
        steps {
           '''
            sh
            #!/bin/bash
            echo $TEST $TEST1
            sleep 5
            '''
        }


   }


 }



}




