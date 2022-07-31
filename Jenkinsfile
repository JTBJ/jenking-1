pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'echo "Hello World"'
                bat '''
                    echo "Multiline shell steps works too"
                    cd ../../../eclipse-workspace/Simple/src/main/java/simple
                    javac Simple.java
                    java Simple.java
                '''
            }
        }
    }
}
