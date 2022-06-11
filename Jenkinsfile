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

}
