pipeline {
  agent any
  stages {
    stage ( 'Git Clone') {
      steps {
      git  'https://github.com/Hemachandra-423/simple-web-app.git'
      }
    }
    stage ( 'Maven Build') {
      steps {
        bat 'mvn clean install'

      }
    }
    stage ( 'unit test') {
      steps {
        echo 'unittest'
      }
    }
    stage ( 'deploy') {
      steps {
deploy adapters: [tomcat8(credentialsId: '67604b6d-1703-403a-bd5f-815f722cada6', path: '', url: 'http://localhost:9595')], contextPath: '/simple-web-app', war: '**/*.war'      }
    }
  }
}