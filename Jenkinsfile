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
            mail(subject: 'Pipeline', body: 'Build OK', from: 'yolande.kamga@sprint-pay.com  ', cc: ' yolande.kamga@sprint-pay.com  ', replyTo: 'yolande.kamga@sprint-pay.com  ')
          }
        }

      }
    }

    stage('Frontend') {
      parallel {
        stage('Frontend') {
          agent any
          steps {
            echo 'test'
          }
        }

        stage('PrepaSonar') {
          steps {
            withSonarQubeEnv(installationName: 'PrepaSonar', credentialsId: 'Sonarqube')
          }
        }

      }
    }

    stage('ActivitÃƒÂ© Stactic') {
      agent any
      steps {
        echo 'test2'
        waitForQualityGate(credentialsId: 'sonarwebhook', abortPipeline: true)
      }
    }

  }
}