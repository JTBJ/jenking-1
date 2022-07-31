pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'echo "Hello World"'
                bat '''
                    echo "Multiline shell steps works too"
                    cd ../../../IdeaProjects/swingPractice/src/basicSwing
                    javac App.java
                    java App.java
                '''
            }
        }
    }
}
