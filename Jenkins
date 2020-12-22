pipeline {
  agent any
  stages {
    stage ( 'Git Clone') {
      steps {
      git  'httpsgithub.comHemachandra-423simple-web-app.git'
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
        deploy adapters [tomcat8(credentialsId '07f9e9cb-69c1-4080-987d-3399d4e9ae3a', path '', url 'httplocalhost9595')], contextPath 'simple-web-app', war '.war'  
		}
  }
}
}