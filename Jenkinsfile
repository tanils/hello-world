pipeline {
  agent any
  stages {
    stage('Source') { // Get code
      steps {
        // get code from our Git repository
        git 'https://github.com/tanils/hello-world.git'
      }
    }
  stage('Compile') { // Compile and do unit testing
      tools {
        Maven 'Maven 3.6.2'
      }
      steps {
        // run Gradle to execute compile and unit testing
        sh 'clean compile test package'
      }
    }
  }
  }
  

