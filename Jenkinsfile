node {

stage('SCM'){
 git 'https://github.com/thomas-martin-adaming/Gestion_Comptable_Back'
}

stage('Compile'){
def mvnHome = tool name: 'maven-3' , type: 'maven'
sh "${mvnHome}/bin/mvn package"
}

stage('SonarQube') {
  def mvnHome = tool name: 'maven-3' , type: 'maven'
  sh "${mvnHome}/bin/mvn sonar:sonar -Dsonar.host.url=http://192.168.0.31:9000"
    }
}
