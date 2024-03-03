pipeline {
      agent any
 
      stages  {
         stage ('CRED'){
          steps {
            // This is accesssing credentials using username and password
              withCredentials([usernamePassword(credentialsId: 'test_up' , usernameVariable: 'USERNAME' , passwordVariable: 'PASS') ] ) {
                echo "$USERNAME $PASS"

                sh '''
                echo "$USERNAME $PASS"
              '''
              }
          
               // This is accesssing credentials using secret text
              withCredentials([string(credentialsId: 'secret_text' , variable: 'SECRET_TEXT') ] ) {
                echo "$SECRET_TEXT"

                sh '''
                echo "$SECRET_TEXT"
              '''
              }
              // This is accesssing credentials using secret file
                withCredentials([file(credentialsId: 'secret_file' , variable: 'FILE_PATH') ] ) {
                 echo "$FILE_PATH"

                sh '''
                cat "$FILE_PATH"
                   '''
              }
            // This is accesssing credentials using ssh username with private key
                withCredentials([sshUserPrivateKey(credentialsId: 'ssh_pem' , usernameVariable: 'USER' , keyFileVariable: 'SSH_KEY') ] ) {
                 echo "$SUSER $SSH_KEY"

                sh '''
                echo "$USER $SSH_KEY"
                   '''
              }
          }
      }  

 }

}     

