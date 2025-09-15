pipeline{
  agent any
  stages{
    stage('checkout SCM'{
      steps{
        branch:'master' ,url:'https://github.com/sandeepsirivella/simpleChatApp--1.git'
      }
    }
    stage('build'){
      steps{
        sh """
        npm install
        npm run build
        """
      }
    }
    stage('deploy'){
      steps{
        sh """
        docker build -t aa:1 .
        docker run -d -p 8070:80 aa:1
        """
      }
    }
  }
post {
        success {
            echo "Deployment completed successfully 🚀"
        }
        failure {
            echo "Pipeline failed ❌"
        }
    }
}
        
