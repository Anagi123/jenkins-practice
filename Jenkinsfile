pipeline {
    agent { node { label 'AGENT-1' } }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                    ls -ltr
                    pwd
                    echo "Hello script"
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // error 'this...failed'
            }
        }
    }
    post { 
        always { 
            echo 'I will always run whether the job is success or not'
        }
    success{
        echo 'I will only when job is success'
    }    
    failure{
        echo 'I will only when job is success'
    }
    }
}
