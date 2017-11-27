pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'Print build'
          }
        }
        stage('code quality') {
          steps {
            echo 'print code quality'
          }
        }
        stage('compile') {
          steps {
            echo 'print compile'
          }
        }
      }
    }
    stage('Deploy to QA') {
      steps {
        echo 'tralala'
      }
    }
    stage('UT') {
      parallel {
        stage('UT') {
          steps {
            echo 'test UT'
          }
        }
        stage('Perf test') {
          steps {
            echo 'perf'
          }
        }
        stage('Secutity Test') {
          steps {
            echo 'security'
          }
        }
      }
    }
    stage('Deploy to PROD') {
      steps {
        echo 'prod'
        input 'GO NO GO change mananager'
      }
    }
  }
}