pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/dave-odun/sample-java-programs', branch: 'master')
      }
    }

    stage('Script') {
      parallel {
        stage('Script') {
          steps {
            sh '''pwd
ls -la'''
          }
        }

        stage('Install Java') {
          steps {
            sh '''brew install java

java --version'''
          }
        }

      }
    }

  }
}