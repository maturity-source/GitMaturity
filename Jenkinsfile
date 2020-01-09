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

        stage('Passer') {
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

    stage('Activité Stactic') {
      steps {
        sh 'echo qualité du code'
      }
    }

  }
}