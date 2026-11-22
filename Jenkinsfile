pipeline {
    agent any
    tools {
        jdk 'JAVA_HOME'
        maven 'M2_HOME'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/KhalilBelouahchia2/4fintech4-KhalilBelouahchia.git'
            }
        }
        stage('Build Maven') {
            steps {
                dir('backend') {
                    sh 'mvn clean package -DskipTests'
                }
            }
        }
        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    dir('backend') {
                        sh 'mvn sonar:sonar -Dsonar.projectKey=4fintech4-KhalilBelouahchia -Dsonar.projectName="4fintech4-KhalilBelouahchia"'
                    }
                }
            }
        }
    }
}
