pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/willerf/maven-samples-A6.git', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh 'mvn clean install'
        sh 'mvn clean'
        sh 'mvn verify'
        sh 'mvn test'
        sh 'git bisect start 198644632661c67b6c32f59e9047c11a70685e15 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5 && git bisect run mvn clean test'
      }
    }
  }
  tools {
    maven 'Maven'
    jdk 'Java'
  }
}
