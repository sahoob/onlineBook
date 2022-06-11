node
{
stage('Cloning Git'){
		git branch: 'main', url: 'https://github.com/sahoob/onlineBook.git'
}
stage('Compile Package and Create war file'){
		 def mvnHome= tool name: 'MAVEN3', type: 'maven'
         def setHomepath= "${mvnHome}/bin/mvn"
         sh "${setHomepath} clean install package"

}

stage('build docker Image') {
      sh 'docker build -t khoka2020/onlinebook:1.0.0 .'

}

stage('push docker Image'){

withCredentials([usernamePassword(credentialsId: '0960f87c-4cda-4448-aa33-e144908b1d2f', passwordVariable: 'docker_pwd', usernameVariable: 'docker_uname')]) {
    sh "docker login -u ${docker_uname} -p ${docker_pwd}"
}

   sh 'docker push khoka2020/onlinebook:1.0.0'


}
stage('run docker container'){

sh 'docker run -p 8085:8085 -d --name onlinebook khoka2020/onlinebook:1.0.0'

}
}
