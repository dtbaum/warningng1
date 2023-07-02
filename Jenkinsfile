pipeline {
  agent {label ''}
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
     stage('Parse Dependency-Check Report') {
      steps {
        // Parsen des Dependency-Check-Berichts mit dem Warnings Next Generation Plugin
        warningsNextGeneration parsers: [[parserName: 'Dependency-Check Parser', parserConfigurations: [[pattern: '/tmp/dependency-check-report.json']]]]
      }
    }
  }
}
