pipeline {

    agent { label "do-not-use-master" }

    stages {
        stage('Run Parallel Tests') {
            parallel {
                stage('Test On Windows') {
                    steps { sh "sleep 10" }
                }
                stage('Test On Linux') {
                    agent {
                        docker { image 'busybox' }
                    }
                    steps { sh "sleep 12" }
                }
                stage('Test On Mac') {
                    steps { sh "sleep 5" }
                }
            }
        }
    }
}
