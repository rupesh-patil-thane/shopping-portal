pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is build the app job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is test the app job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is package the app job'
        sh 'npm run package'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'This pipeline has completed...'
    }

  }
}