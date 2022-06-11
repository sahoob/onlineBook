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
         withMaven(maven : 'ápache-maven-3.8.5'){
        sh 'mvn clean install package'
         }
      }
    }
   
}
}
