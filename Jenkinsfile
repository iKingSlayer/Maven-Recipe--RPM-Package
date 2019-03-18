
pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /${user.home}/.m2:/{user.home}/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
              sh 'mvn -v'
              sh 'mvn -B -DskipTests clean package'
            }
       }
    }
}
