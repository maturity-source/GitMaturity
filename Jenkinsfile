pipeline {
  agent any
  stages {
    stage('Buid') {
      steps {
        sh 'echo pour passer un build'
      }
    }

    stage('Backend') {
      parallel {
        stage('Backend') {
          steps {
            sh 'echo pour le back'
          }
        }

        stage('') {
          steps {
            sh 'on teste le back'
          }
        }

      }
    }

    stage('Frontend') {
      steps {
        sh 'echo C\'est pour le Front'
      }
    }

    stage('Activit� Stactic') {
      steps {
        sh 'echo qualit� du code'
      }
    }

  }
}