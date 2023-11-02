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
            sh '''mvn -s ./settings.xml package
echo "aaaa"
echo "bbbb"'''
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
    stage('print2') {
      steps {
        println 'aaaaaaabbbbbbcccaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaabbbb'
      }
    }

  }
  environment {
    release_env = '1.0.0'
  }
}
