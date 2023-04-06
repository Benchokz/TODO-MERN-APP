pipeline {
  agent any
  stages {
    stage('Log tool versions') {
      steps {
        sh 'git --version'
      }
    }

    stage('Build with maven') {
      steps {
        sh 'mvn compile test package'
      }
    }

    stage('Post build step') {
      steps {
        writeFile(file: 'Status.txt', text: 'Hi, it works fine')
      }
    }

  }
}