pipeline { 
    agent any 
    stages { 
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM',
                branches: [[name: '*/main']]
                userRemoteConfigs: [[url: 'https://github.com/Vishal-Srinivasa/PES1UG22CS701_Jenkins.git']]])
            }
        }
        stage('Build') { 
            steps {
                build 'PES1UG22CS701-1' 
                sh 'g++ main.cpp -o output'
            } 
        } 
        stage('Test') { 
            steps { 
                sh './output'
            } 
        } 
        stage('Deploy') { 
            steps { 
                echo 'deploy' 
            } 
        } 
    }
    post { 
        failure { 
            echo 'Pipeline failed' 
        }
    }
} 