pipeline {
    agent any

    stages  {
    stage ('Build'){
        environment {
         BUILD_NAME = "my_build"
        }
        steps {
           
            sh '''
            sleep 10
            echo $TEST $BUILD_NAME
            '''
    }
        
}
    stage ('Test'){
        steps {
          sh '''
            #!/bin/bash
            echo $TEST $BUILD_NAME
            sleep 5
            '''
        }


   }


 }



}




