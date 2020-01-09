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
            build(job: 'sonartest', quietPeriod: 1)
          }
        }

      }
    }

    stage('Backend') {
      parallel {
        stage('Backend') {
          agent any
          steps {
            echo 'salut'
          }
        }

        stage('qualité') {
          steps {
            mail(subject: 'essai', body: 'test', to: 'yolande.kamga@sprint-pay.comyolande.kamga@sprint-pay.com', from: 'happymaturity@gmail.com', bcc: 'yolandekegne@yahoo.fr', cc: 'happymaturity@gmail.com', replyTo: 'yolandekegne@yahoo.fr')
          }
        }

      }
    }

    stage('Frontend') {
      agent any
      steps {
        echo 'test'
      }
    }

    stage('ActivitÃƒÂ© Stactic') {
      agent any
      steps {
        echo 'test2'
      }
    }

  }
}