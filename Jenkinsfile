@Library('jenkins-poc-shared-lib') _

def isProd = "${env.JOB_NAME.split('/')[1]}" == "prod"
def autoConfirmParam = isProd ? [] : [booleanParam(name: 'AutoConfirm', defaultValue: "", description: 'Auto Confirm Terraform apply')]

// BEGIN Jenkins job parameters menus
properties([
    parameters([
        booleanParam(name: 'PopulateParameters', defaultValue: false, description: 'Select to populate this job parameters'), 
        choice(name: 'Env', choices: ["${env.JOB_NAME.split('/')[1]}"], description: 'This Jenkins Job base name must using one of these valid environments: nonprod, stag or prod'),
        choice(name: 'Region', choices: ['virginia'], description: ''),
        choice(name: 'Color', choices: ['','blue','green'], description: 'The color off the stock'),
        string(name: 'Branch', defaultValue: 'master', description: 'The branch of the build'),
        string(name: 'BuildNumber', defaultValue: '', description: 'The build number of the app package'),
        choice(name: 'Action', choices: ['plan','apply','destroy'], description: 'Terraform action for this job'),
        autoConfirmParam,
    ].flatten())
    ])

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
