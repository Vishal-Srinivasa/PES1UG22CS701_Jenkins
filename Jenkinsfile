pipeline {
  agent any
  
  stages {
    stage('Build'){
      steps{
        sh 'g++ -o PES1UG22CS701-1 main.cpp'
        echo "Build Successful"
      }
    }
    
    stage('Test'){
      steps{
        sh './PES1UG22CS701-1'
        echo "Test Successful"
      }
    }
    
    stage('Deploy'){
      steps{
        eco "Deployment Successful"
      }
    }
  }
  
  post{
    failure{
      echo "Pipeline Failed"
    }
  }
}

