pipeline {
  agent any
  stages {
    stage('build job1') {
      parallel {
        stage('build job1') {
          steps {
            build 'test_blue_ocean'
          }
        }

        stage('buildjob2') {
          steps {
            build 'test_blue_ocean2'
          }
        }

        stage('shell') {
          steps {
            sh 'echo "12345"'
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
  environment {
    release_env = '1.0.0'
  }
}