pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Jar') {
            steps {
                bat '''
                javac Main.java
                jar cfe MyApp.jar Main Main.class
                '''
            }
        }

        stage('Run Jar') {
            steps {
                bat 'java -jar MyApp.jar'
            }
        }
    }
}
