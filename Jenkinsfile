pipeline {
  agent any
  stages {
    stage('iniciar') {
      steps {
        sh '''printenv
ls
'''
        sh 'echo "Hola $nombre"'
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