pipeline{
    agent any

    environment{
        stagging_server="178.33.224.29"
    }

    stages{
        stage('Deploy to Remote'){
            steps{
                sh 'scp ${WORKSPACE}/* root@${stagging_server}:/home/yellowsoft/public_html/projects/jenkinstest'
            }
        }
    }
}
