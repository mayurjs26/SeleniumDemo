node {
	stage ('SCM checkout'){
		echo 'start SCM checkout'
		git "https://gitlab.com/mbabilo/expiritest"
		echo 'Step complete'
		}
	stage ('Build'){
    	dir("comtest") {
       sh "pwd"
       echo 'start Build'
	   sh "mvn clean install"
	   echo 'Step mvn clean install is done'
       }
       	dir("comtest/target") {
       sh "pwd"
	   echo 'Step java -jar is started'
	   sh "java -jar com.test-1.0-SNAPSHOT.jar"
	   echo 'Step java -jar is done'
       }
		}
}