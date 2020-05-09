pipeline {
    agent {docker { image 'node:6.3' }}
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm start'
            }
        }
 	stage('Sanity check') {
            steps {
                input "Does the staging environment look ok?"
            }
        }
        stage('Deliver') { 
            steps {
                print('done')
            }
        }
    }
    
post {
    failure {
        mail to: 'bakhromovkhurshid@gmail.com',
             subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
             body: "Something is wrong with ${env.BUILD_URL}"
        }
    }
}
