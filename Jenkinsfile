pipeline {
  agent any
  tools { 
      maven 'MAVEN_HOME' 
      jdk 'JAVA_HOME' 
  }
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/dhetong/maven-samples-A6.git', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh 'mvn verify'
      }
    }

  }
}
