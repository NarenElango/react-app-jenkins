pipeline {
     agent any 
	stages {
        stage("Build") {
            steps {
                sh "npm install"
                sh "npm run build"
            }
        }
		
        stage("Deploy to"){
            steps { 
                sh " sudo rm -rf /var/www/html/*"
                sh " sudo cp -r /var/lib/jenkins/workspace/react-app/dist/* /var/www/html/"
            }
        }
        
    }
}
