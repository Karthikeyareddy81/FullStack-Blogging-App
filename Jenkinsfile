pipeline { 
    agent any
    environment {
        KUBECONFIG = credentials('d70c2669-99a6-4ad1-888a-f59569225763')
        SERVICE-ACCOUNT = credentials('388e1123-d4a9-4ff1-a836-ba5805ae6c6a')
    }
    
    tools {
        maven 'maven3'
        jdk 'jdk17'
    }

    stages {
        
        stage('Compile') {
            steps {
            sh  "mvn compile"
            }
        }
        
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        
        stage('Package') {
            steps {
                sh "mvn package"
            }
        }
    }
}
