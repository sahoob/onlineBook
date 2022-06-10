pipeline {
   agent any

  stages {
    stage('Cloning Git') {
      steps {
        git 'https://github.com/sahoob/onlineBook.git'
      }
    }
    stage('Compile Package and Create war file') {
      steps {
        sh "mvn package"
      }
    }
   
}
}
