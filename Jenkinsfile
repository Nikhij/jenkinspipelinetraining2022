pipeline {

agent any

stages {
	stage('SCM') {
		steps  {
			echo "git pull my code for java app"
			https://github.com/jenkins-docs/simple-java-maven-app.git
		}
	}

	stage('Build') {
		steps { 
			sh 'mvn clean package'
		}
	}	

	stage('Deploy') {
		steps {
			sh 'java -jar target/*.jar'
		}
	}

	stage('Deploy to Prod') {
		steps {
			echo "my final webapp to prod"
		}
	}

}

}
