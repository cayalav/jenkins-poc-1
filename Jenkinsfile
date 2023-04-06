@Library('jenkins-poc-shared-lib') _

pipeline {
  agent any
  stages {
    stage('Hello World') {
      steps {
        helloWorld(name:"Carlos", projectName:"jenkins-poc-1")
        helloWorldSimple("Carlos","jenkins-poc-1")
        helloWorldExternal(name:"Carlos", projectName:"jenkins-poc-1")
      }
    }
  }
}
