pipeline {
  agent any
  stages {
    stage('Buid') {
      parallel {
        stage('Buid') {
          steps {
            echo 'soimple'
          }
        }

        stage('Essai') {
          steps {
            fileExists 'pom.xml'
          }
        }

      }
    }

    stage('Backend') {
      agent any
      steps {
        echo 'salut'
      }
    }

    stage('Frontend') {
      agent any
      steps {
        echo 'test'
      }
    }

    stage('ActivitÃ© Stactic') {
      agent any
      steps {
        echo 'test2'
      }
    }

  }
}