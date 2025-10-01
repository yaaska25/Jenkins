pipeline {
    agent any

    environment {
        SONAR_SCANNER_HOME = 'C:/sonar-scanner-5.0.1.3006-windows/bin'
        SONAR_HOST_URL = 'http://localhost:9000'
        SONAR_PROJECT_KEY = 'MOHAMED'
        SONAR_LOGIN = 'sqa_98985d998ed2d7d0b58deb358ffc642b8108ac10'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/yaaska25/Jenkins.git'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('MySonarQube') {
                   bat 'C:\\sonar-scanner-5.0.1.3006-windows\\bin\\sonar-scanner -Dsonar.projectKey=MOHAMED -Dsonar.sources=src -Dsonar.host.url=http://localhost:9000 -Dsonar.login=sqa_98985d998ed2d7d0b58deb358ffc642b8108ac10'
                }
            }
        }
    }
}
kk
