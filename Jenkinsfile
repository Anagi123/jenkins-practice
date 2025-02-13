pipeline {
    agent { node { label 'AGENT-1' } }
    options{
        timeout(time: 1,unit: 'HOURS')
    }

    // triggers{
    //     cron('* * * * *')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                    ls -ltr
                    pwd
                    echo "Hello script from github push web-hook event"
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
