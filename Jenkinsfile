pipeline {
      agent any
 
      stages  {
         stage ('Checkout'){
          steps {
              withCredentials([usernamePassword(credentialsId: 'test_up' , usernameVariable: 'USERNAME' , passwordVariable: 'PASS') ] ) {
                echo $USERNAME $PASS

                sh '''
                echo "$USERNAME $PASS"
              }

          }
      }  
 }

}     

