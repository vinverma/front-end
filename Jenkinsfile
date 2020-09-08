pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'compiling and Building..'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'Running Test cases'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'Packaging....'
        sh 'npm run package'
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
}