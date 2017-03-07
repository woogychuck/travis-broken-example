node {
   
   def scannerHome
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      git https://github.com/HankQuiter/travis-broken-example.git
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configureddeleteDir()
      // **       in the global configuration.           
      scannerHome = tool 'SonarScanner';
   }
   stage('SonarQube analysis') {
        withSonarQubeEnv('Cloud Machine') {
        sh "${scannerHome}/bin/sonar-scanner"
    }
   }

}

