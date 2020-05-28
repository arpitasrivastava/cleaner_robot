pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo \'123\''
      }
    }

    stage('test') {
      steps {
        sh 'echo \'tests\''
      }
    }

    stage('alpha') {
      steps {
        sh 'echo \'alpha\''
      }
    }

    stage('beta') {
      steps {
        sh 'echo \'beta\''
      }
    }

    stage('gamma') {
      steps {
        sh 'echo \'gamma\''
      }
    }

    stage('prod monitor') {
      parallel {
        stage('prod monitor') {
          steps {
            sh 'echo \'prod monitor\''
            sh '''/usr/local/bin/python3 /Users/sarpit/PycharmProjects/woody/xyz.py
'''
          }
        }

        stage('prod server 1') {
          steps {
            sh 'echo \'prod server 1\''
          }
        }

        stage('prod server 2') {
          steps {
            sh 'echo \'prod server 2\''
          }
        }

      }
    }

  }
}