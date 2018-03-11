pipeline {
  agent none
  stages {
    stage('Build') {
      parallel {
        stage('Static HTML') {
          steps {
            echo 'Build Phase'
            git(url: 'https://github.com/dagen/resume.git', branch: 'development', changelog: true)
          }
        }
        stage('Test') {
          steps {
            echo 'Testing'
            readFile './index.html'
          }
        }
      }
    }
  }
}