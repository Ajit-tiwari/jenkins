node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
      def scannerHome = tool 'SonarScanner';
      withSonarQubeEnv(credentialsId: 'sonartoken') {
        sh "${scannerHome}/bin/sonar-scanner"
      }
  }
}
