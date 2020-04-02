pipeline {
  agent any
  stages {
    stage('clonegit') {
      steps {
        git(url: 'https://github.com/darealmc/some_java.git', branch: 'pipeline')
      }
    }

    stage('') {
      steps {
        withAnt(installation: 'ant_1') {
          sh 'ant clean junit'
        }

      }
    }

    stage('testing') {
      steps {
        junit 'test/results/*.xml'
      }
    }

  }
}