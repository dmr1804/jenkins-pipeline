pipeline{
  agent any
       tools{
        maven 'LocalMaven'
    }
  stages {
    stage("SCM Checkout"){
            steps{
            git 'https://github.com/dmr1804/jenkins-pipeline.git'
            
            }
        }
    
        stage("Clean repo"){
          steps{
            withMaven(maven: 'LocalMaven') {
            bat 'mvn clean'
            }
            }
       }
        
    stage("Clean test"){
          steps{
            withMaven(maven: 'LocalMaven') {
            bat 'mvn test'
            }
            }
       }
    
    stage('Maven install') {
      steps {
         withMaven(maven: 'LocalMaven') {
          bat 'mvn install'
}
    }
  }
}
}
