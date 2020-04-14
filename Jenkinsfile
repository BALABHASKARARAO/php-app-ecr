node {
  stage 'Checkout'
  git url: 'https://github.com/balaguntupalli/php-app-ecr.git'
 
  stage 'Docker build'
  docker.build('demo')
 
  stage 'Docker push'
  docker.withRegistry('861614002005.dkr.ecr.us-east-1.amazonaws.com', 'ecr:us-east-1:ecr-cred') {
    docker.image('demo').push('latest')
  }
}
