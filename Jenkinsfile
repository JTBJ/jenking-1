pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'echo "Hello World"'
                bat '''
                    echo "Multiline shell steps works too"
                    cd ../../../IdeaProjects/swingPractice/src/selfPractice
                    javac Main.java
                    java Main.java
                '''
            }
        }
    }
}
