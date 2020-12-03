pipeline {
  agent {
                docker { image 'node:14-alpine' }
  }
  stages {
    stage('Cloning Git') {
      steps {
        git 'https://github.com/sanjeevkumarrao/node-hello-world'
      }
    }
    stage('Build') {
       steps {
         sh 'npm install'
       }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
  }
}
