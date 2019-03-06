node {
	stage ('SCM checkout'){
		git "https://gitlab.com/mbabilo/expiritest"
		}
	stage ('Build'){
    	dir("comtest") {
       sh "pwd"
	   sh "mvn clean install"
       }
       	dir("comtest/target") {
       sh "pwd"
	   sh "java -jar com.test-1.0-SNAPSHOT.jar"
       }
		}
}