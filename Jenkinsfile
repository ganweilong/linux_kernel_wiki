pipeline {
  agent any
  stages {
    stage('build job1') {
      parallel {
        stage('build job1') {
          steps {
            //build 'test_blue_ocean'
            build job: 'test_blue_ocean', parameters: [string(name: 'release_env', value: 'aaaaabbb'), string(name: 'release_version', value: '1.0.2')]
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
      agent any
      steps {
        echo 'aaaaaaabbbbbbcccaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaabbbb'
      }
    }

  }
  environment {
    release_env = '1.0.0'
  }
}
