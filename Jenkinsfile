node {
  stage 'Checkout'
  git url: 'https://github.com/balaguntupalli/php-app-ecr.git'
 
  stage 'Docker build'
  docker.build('php-app')
 
  stage 'Docker push' {
      steps {
          script {
              docker.withRegistry('861614002005.dkr.ecr.us-east-1.amazonaws.com', 'ecr:us-east-1:ecr-cred') {
              docker.image('php-app').push('latest')
            }
        }
   }
}
