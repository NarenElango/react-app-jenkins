pipeline {
     agent any 
	stages {
        stage("Build") {
            steps {
                sh "npm install"
                sh "npm run build"
            }
        }
        stage("Deploy"){
            steps { 
                sh "rm -rf /var/www/html/*"
                sh "cp -r ${WORKSPACE}/react-app/dist/* /var/www/html/"
            }
        }
        
    }
}
