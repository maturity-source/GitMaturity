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

        stage('git') {
          steps {
            jacoco(buildOverBuild: true, changeBuildStatus: true, maximumMethodCoverage: '100', minimumBranchCoverage: '80', minimumClassCoverage: '80', minimumComplexityCoverage: '80', minimumInstructionCoverage: '80', minimumLineCoverage: '80', minimumMethodCoverage: '80', deltaBranchCoverage: 'master', deltaClassCoverage: 'all', maximumLineCoverage: '80', maximumInstructionCoverage: '80', maximumComplexityCoverage: '100', maximumClassCoverage: '100', maximumBranchCoverage: '80', classPattern: '\'target/classes\'', execPattern: '\'target/classes\'', sourceExclusionPattern: '\'src/test*\'')
          }
        }

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