pipeline {
    agent any

    environment {
        JAVA_HOME = "/usr/lib/jvm/java-21-openjdk-amd64"
        PATH = "${JAVA_HOME}/bin:${env.PATH}"
        DOCKER_IMAGE = "satyendragit123/springboot-app:v1"
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    credentialsId: 'github-creds',
                    url: 'https://github.com/satyendragit123/Jenkins150626.git'
            }
        }

        stage('Build') {
            steps {
                sh '''
                echo "JAVA_HOME=$JAVA_HOME"
                java -version
                javac -version
                mvn -version
                mvn clean package
                '''
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
