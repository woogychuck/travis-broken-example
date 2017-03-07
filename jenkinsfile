node {
  stage('SCM') {
    git 'https://github.com/HankQuiter/travis-broken-example.git'
  }
  stage('SonarQube analysis') {
    // requires SonarQube Scanner 2.8+
    def scannerHome = tool 'SonarQube Scanner 2.8';
    withSonarQubeEnv('My SonarQube Server') {
      sh "/opt/sonarqube-6.2/sonar_scanner/bin/sonar-scanner"
    }
  }
}
