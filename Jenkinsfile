pipeline {
    agent none

    stages  {
    stage ('Build'){
         agent {
        label 'install_jenkin'
    }
        steps {
            sh 'sleep 5'
    }
        
}
    stage ('Test'){
        agent any
        steps {
            sh '''
            #!/bin/bash
            ls -lrt
            sleep 5
            '''
        }


   }


 }



}




