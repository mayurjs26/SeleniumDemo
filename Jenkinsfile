node {
	stage ('SCM checkout'){
		git credentialsId: '516478bc-ed54-433e-9c73-38bf463d316e', url: 'https://gitlab.com/mbabilo/experitest.git'
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