pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building..'
            sh 'hostname'
            sh 'pwd'
            sh 'ls -al && hostname && pwd && cat /etc/passwd'
          }
        }

        stage('error') {
          steps {
            sh 'ls -al'
          }
        }

        stage('teststage') {
          steps {
            sh 'ls -al'
          }
        }

      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Testing..'
          }
        }

        stage('error') {
          steps {
            sleep 10
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }

  }
}
