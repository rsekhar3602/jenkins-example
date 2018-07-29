

pipeline {
    node {
   def mvnHome
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/rsekhar3602/jenkins-example.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      mvnHome = 'C:/Installations_devops/apache-maven-3.0.5'
   }
   }

    stages {
        stage ('Compile Stage') {
              bat(/"${mvnHome}\bin\mvn" clean package/)
            }
        }
		

        stage ('Testing Stage') {
           bat(/"${mvnHome}\bin\mvn" test/)
        }


        stage ('Deployment Stage') {
      bat(/"${mvnHome}\bin\mvn" deploy/)
    }
	}

}

}
