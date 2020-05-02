// Declarative pipeline
pipeline {
    agent any
    
    stages {
	    
	stage('BUILD') {
            steps {
		echo 'Building..'    
                sh '''
		   cd /home/ubuntu/project/
		   pwd
		   ansible node -m ping
		...   
	    }
        }
	stage('Compile Stage') {
            steps {
                sh "mvn clean compile"
            }
        }
        stage('Package') {
            steps {
                sh "mvn package"
            }
        }
        stage('Deploy') {
            steps {
                sh "mvn tomcat:redeploy"
            }
	}
    }
    post {
        failure {
            script {
                currentBuild.result = 'FAILURE'
            }
        }

        always {
            step([$class: 'Mailer',
                notifyEveryUnstableBuild: true,
                recipients: "duvva.raghavendra@gmail.com",
                sendToIndividuals: true])
        }
    }
} 
