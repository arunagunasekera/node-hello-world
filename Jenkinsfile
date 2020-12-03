pipeline {
  agent any
  stages {
    stage('Cloning Git') {
      steps {
        git 'https://github.com/arunagunasekera/node-hello-world.git'
      }
    }
    stage('Build') {
       steps {
         sh 'npm install'
       }
    }
    stage('Test') {
      steps {
        sh 'npm run test'
      }
    }
    stage('package'){
        steps{
            sh 'git config --global user.email "the.aruna@gmail.com"'
            sh 'git config --global user.name "Aruna"'
            sh "npm version 0.0.$BUILD_NUMBER"
            sh 'npm pack'
            sh 'cp Hello-World-0.0.$BUILD_NUMBER.tgz /jenkins/artifact-repository'
        }
    }
    stage('deploy'){
        steps{
            sh 'cd /jenkins/deployment && npm install /jenkins/artifact-repository/Hello-World-0.0.$BUILD_NUMBER.tgz'
        }
    }

  }
}
