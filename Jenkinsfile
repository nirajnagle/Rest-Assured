
node{
    stage ('git checkout'){
    	sh 'ls -ltr'
    	checkout scm
    	sh 'ls -ltr'
    	echo 'inside jenkins'
	sh 'whoami'    
    	sh 'docker images'
        def customImage = docker.build("restassure-demo:${env.BUILD_ID}")
	sh 'docker images'
        customImage.inside {
	sh 'pwd'
        sh 'ls -ltr'
	sh 'tar -cvf name.tar .'
        }
    }
}
