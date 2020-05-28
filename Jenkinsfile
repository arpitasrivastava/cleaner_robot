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
        sh 'python deploy --host_name=alpha --package=irona'
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
  environment {
    python_home = '/usr/local/bin/python3'
    deploy = '/Users/sarpit/PycharmProjects/woody/main.py'
    alpha = 'ALPHA'
    beta = 'BETA'
    gamma = 'GAMMA'
    prod_monitor = 'PROD_MONITOR'
    prod_server_1 = 'PROD_SERVER_1'
    prod_server_2 = 'PROD_SERVER_2'
  }
}