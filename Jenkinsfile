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
      //tools {
        //Maven 'Maven 3.6.2'
      //}
      steps {
        // run Gradle to execute compile and unit testing
        sh 'mvn clean compile test package'
      }
    }
  
    stage('mail'){
      steps{
        mail bcc: 'anil.tammali198703@gmail.com', body: 'build success', cc: 'anil.tammali198703@gmail.com', from: '', replyTo: '', subject: 'build sucess', to: 'anil.tammali198703@gmail.com'
      }
      }
  
  }
}
  

