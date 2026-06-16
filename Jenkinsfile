environment {
    JAVA_HOME = "/usr/lib/jvm/java-21-openjdk-amd64"
    PATH = "${JAVA_HOME}/bin:${env.PATH}"
    DOCKER_IMAGE = "satyendragit123/springboot-app:v1"
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
