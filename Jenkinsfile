@Library('jenkins-poc-shared-lib') _

pipeline {
  agent any
  stages {
    stage('Hello World') {
      steps {
        helloWorld(name:"Carlos", dayOfWeek:"Juernes")
        helloWorldSimple("Carlos","Juernes")
      }
    }
  }
}
