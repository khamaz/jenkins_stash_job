pipeline {
  agent any
  stages {
    stage ('create files') {
      steps {
        sh '''
        touch file.txt
        mkdir -p target
        touch target/file2.jar
        touch target/file3.war
        tree
        '''
      }
    }
  }
}
