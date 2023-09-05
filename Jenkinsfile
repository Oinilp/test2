pipeline {
  agent any
  stages {
    stage('step1') {
      steps {
        git(url: 'https://github.com/Oinilp/test2.git', branch: 'main')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -al'
          }
        }

        stage('test') {
          steps {
            sh 'cd src && npm install && npm run start'
          }
        }

      }
    }

  }
}