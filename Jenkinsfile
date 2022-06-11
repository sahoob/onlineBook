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
        
        sh '/opt/apache-maven-3.8.5/bin/mvn clean install package'
      
      }
    }
   
}
}
