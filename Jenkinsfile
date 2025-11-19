pipeline {
    agent any
    environment {                   // Use machine's path
               PATH = "/opt/maven/bin:${env.PATH}"
    }
    stages {                                  //stages where we can mention build.,test,
        stage('Build') {
            steps {                     
              sh "mvn clean package -Dmaven.test.failure.ignore=true "
                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
            }
    }
}
