pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'apache-maven-3.0.5') {
                    bat 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {
            steps {

            withMaven(maven : 'apache-maven-3.0.5') {
                    bat 'mvn test'
            }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'apache-maven-3.0.5') {
                    bat 'mvn deploy'
                }
            }
        }
    }

}
