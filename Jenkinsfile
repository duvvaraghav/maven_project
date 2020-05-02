// Declarative pipeline
pipeline {
    agent any
    
    stages {
	stage('Ansible') {
	  ansibleplaybook (
              colorized: true
	      become: true
	      inventory: 'hosts.yml
	 }
    }
}		  
