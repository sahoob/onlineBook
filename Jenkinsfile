pipeline {
   agent any

  stages {
    stage('Cloning Git') {
      steps {
        git branch: 'main', url: 'https://github.com/sahoob/onlineBook.git'
      }
    }
    stage('Compile Package and Create war file') {
      steps {
         def mvnHome= tool name: 'MAVEN3', type: 'maven'
         def setHomepath= "${mvnHome}/bin/mvn"
         sh "${setHomePath} clean install package"
      
      }
    }
   
}
}
