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
        stash(name: 'myStash')
      }
    }
    stage ('check the file') {
      steps {
        unstash 'myStash'
        sh 'tree'
      }
    }
  }
}
