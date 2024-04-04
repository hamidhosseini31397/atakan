pipeline {
    agent any
    stages {
        stage('Build test hamid') {
            steps {
                script {
                    // Navigera till TrailrunnerProject-mappen
                    dir('TrailrunnerProject') {
                        sh 'mvn compile'
                    }
                }
            }
        }
 
        stage('Test') {
            steps {
                script {
                    // Navigera till TrailrunnerProject-mappen
                    dir('TrailrunnerProject') {
                        sh 'mvn test'
                    }
                }
            }
        }
 
        stage('Post Test') {
            steps {
                script {
                    // Navigera till TrailrunnerProject-mappen
                    dir('TrailrunnerProject') {
                        // Kör junit-kommandot för att läsa in testrapporter
                        junit '**/TEST*.xml'
                    }
                }
            }
        }
    }
}
