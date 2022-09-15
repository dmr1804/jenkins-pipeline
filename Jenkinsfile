pipeline{
  agent any
  stages {
    stage('Maven install') {
      steps {
        withMaven(maven: 'LocalMaven') {
          sh 'mvn test'
}
    }
  }
}
}
