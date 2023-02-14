pipeline {
  agent any 
  stages {
    stage('Build') {
      steps {
          sh 'g++ -o PES1UG20CS672 PES1UG20CS672.cpp'
          build job: 'PES1UG20CS672-1'
      }
    }
    
    stage('Test') {
      steps {
        sh './PES1UG20CS672'
      }
    }
    
    stage('Deploy') {
      steps {
          echo 'Success'
      }
    }
  }
  
  post {
    failure {
      echo "Ohh no!!..Pipeline failed!!.."
    }
  }
}
