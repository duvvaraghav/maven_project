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
		    pwd
		    sudo mkdir duvva
		    ansible node -m ping
		    mkdir duvva
                 '''
             }
        }
    }
}
