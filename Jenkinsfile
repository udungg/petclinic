pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
        snykSecurity(
          snykInstallation: 'snyk-latest',
          snykTokenId: 'Snyk-Jenkins',
          // place other optional parameters here, for example:
          //additionalArguments: '--all-projects --detection-depth=<DEPTH>'
        )
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
  }
}
