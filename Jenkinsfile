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
