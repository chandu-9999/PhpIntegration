pipeline{
    agent any

    environment{
        stagging_server="178.33.224.29"
    }

    stages{
        stage('Deploy to Remote'){
            steps{
                sh ***
                    for fileName in `find ${WORKSPACE} -type -f mmin -10 | grep -v ".git" | grep -v "Jenkinsfile"`
                    do 
                        fil=$(echo ${fileName} | sed 's/'"${JOB_NAME}"'/ /' | awk {'print $2'})
                        scp -r ${WORKSPACE}${fil} root@${stagging_server}:/home/yellowsoft/projects/jenkinstest${fil}
                    done
                ***
            }
        }
    }
}
