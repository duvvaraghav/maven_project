// Declarative pipeline
pipeline {
    agent none

    stages {
	stage('Setting the variables values') {
            agent any		
            steps {
           	 sh '''
                    #!/bin/bash
                    echo "hello world"
		    cd /home/ubuntu/project/
		    ansible node -m ping
                 '''
             }
        }
    }
}
