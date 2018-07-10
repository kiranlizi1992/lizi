pipeline {
  agent any
  environment {
    PATH = '/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games:/snap/bin:/usr/local/apache-ant-1.10.4/bin'
  }

  stages {
    stage('Test') {
      steps {
	sh 'ant test'
      }
    }
    stage('Build') {
      steps {
        sh 'ant build'
      }
    }
    stage('Deploy') {
      steps {
        sh 'cp target/*.jar /tmp'
      }
    }
  }
}

