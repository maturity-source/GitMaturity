pipeline {
  agent any
  stages {
    stage('Buid') {
      steps {
        echo 'soimple'
      }
    }

    stage('Backend') {
      agent any
      steps {
        sh ' pour le back'
      }
    }

    stage('Frontend') {
      agent any
      steps {
        sh 'C\'est pour le Front'
      }
    }

    stage('ActivitÃ© Stactic') {
      agent any
      steps {
        sh 'Qualité du code'
      }
    }

  }
}