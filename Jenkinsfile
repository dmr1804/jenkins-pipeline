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
            bat 'mvn clean
            }
       }
        
    stage("Clean test"){
          steps{
            bat 'mvn test'
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
