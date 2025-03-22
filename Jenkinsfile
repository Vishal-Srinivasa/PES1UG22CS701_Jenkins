pipeline {
  agent any
  
  stages {
    stage('Build'){
      steps{
        build 'PES1UG22CS701-1'
        sh 'g++ -o output main.cpp'
        echo "Build Successful"
      }
    }
    
    stage('Test'){
      steps{
        sh './output'
        eco "Test Successful"
      }
    }
    
    stage('Deploy'){
      steps{
        echo "Deployment Successful"
      }
    }
  }
  
  post{
    failure{
      echo "Pipeline Failed"
    }
  }
}

