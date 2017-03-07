node {
   def scannerHome
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      git https://github.com/HankQuiter/travis-broken-example.git
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      scannerHome = tool 'SonarQube Scanner 2.8';
   }
   stage('SonarQube analysis') {
        withSonarQubeEnv('Cloud Machine') {
        sh "${scannerHome}/bin/sonar-scanner"
    }
   }

}

