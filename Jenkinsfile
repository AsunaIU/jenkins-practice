pipeline {
    agent any
    stages {
        stage('Disk Info') {
            steps {
                echo "Disk state"
                sh 'df -h'
            }
        }
        stage('Top Memory Process') {
            steps {
                echo "Top memory process"
                sh "ps -eo pid,comm,%mem,rss --sort=-%mem | head -n 2 | tail -n 1"
            }
        }
    }
    post {
        always {
            echo "Pipeline finished"
        }
    }
}
