pipeline{
  agent any
  stages {
    stage('Maven install') {
      steps {
        withMaven(maven: 'LocalMaven') {
          sh 'mvn install -Dmaven.javadoc.skip=true -Dgpg.skip'
}
    }
  }
}
}
