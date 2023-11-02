pipeline {
  agent any
  stages {
    stage('build job1') {
      parallel {
        stage('build job1') {
          steps {
            build(job: 'test_blue_ocean', wait: true)
          }
        }

        stage('buildjob2') {
          steps {
            build(job: 'test_blue_ocean2', wait: true)
          }
        }

      }
    }

    stage('print') {
      agent any
      steps {
        echo 'aaaaaaabbbbbbccc'
      }
    }

  }
}