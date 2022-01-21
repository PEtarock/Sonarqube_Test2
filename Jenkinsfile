//Jenkins pipeline script
//Groovy script 

node{
  def mavenHome = tool name: 'maven3.8.4'
  stage('CodeClone') {
    git credentialsId: 'git', url: 'https://github.com/PEtarock/Sonarqube_Test.git'
  }
 /* 
  stage('mavenBuild') {
    sh "${mavenHome}/bin/mvn clean package"
  }
 */
  stage('CodeQuality') {
    sh "${mavenHome}/bin/mvn sonar:sonar"
  // execute the CodeQuality report with sonar
  }

}