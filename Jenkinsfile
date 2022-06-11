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
        def mvnhome= tool 'M2_HOME'
        sh "${mvnhome}/bin/mvn clean install package"
      
      }
    }
   
}
}
