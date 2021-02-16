pipeline {
  agent any
  stages {
    stage('iniciar') {
      steps {
        echo 'Hola mundo'
        sh '''printenv
ls
'''
      }
    }

    stage('crear nuevo archivo') {
      steps {
        writeFile(file: 'mitest.txt', text: 'Nuestro inicio en Jenkins')
        archiveArtifacts '*.txt'
      }
    }

  }
  environment {
    nombre = 'paola'
  }
}