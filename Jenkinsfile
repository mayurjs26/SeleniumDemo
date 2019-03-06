node {
	stage ('SCM checkout'){
	    checkout([$class: 'GitSCM', branches: [[name: '*/master']], 
        userRemoteConfigs: [[url: 'https://gitlab.com/mbabilo/experitest.git']]])
		}
	stage ('Build'){
    	dir("comtest") {
	   sh "mvn clean install"
       }
       	dir("comtest/target") {
	   sh "java -jar com.test-1.0-SNAPSHOT.jar"
       }
		}
}