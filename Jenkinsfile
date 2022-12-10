pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'hello world'
            }
        }
    }

    post {
        changed {
            echo 'pipeline post changed'
        }

        always {
            echo 'pipeline post always'
        }

       success {
            echo 'pipeline post success'
       }
    }

}