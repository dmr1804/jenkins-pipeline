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
    stage('Maven install') {
      steps {
        withMaven(maven: 'LocalMaven') {
          sh 'mvn install -Dmaven.javadoc.skip=true -Dgpg.skip'
}
    }
  }
}
}
