pipeline {
  
  agent any
  parameters {
    choice(name: 'VERSION', choices: ['1.1.0','1.2.0','1.3.0'],description: '')
    booleanParam(name: 'executeTests', defaultValue: true, description: '')
  }
  //tools {
    //maven 'Maven' 
  //}
  //environment {
    //NEW_VERSION = '1.1.0'
    //SEVER_CRDENTIALS = credentials('server-credentials')
  }
  stages {
    
    stage("build") {

      steps {
        echo 'building the application ...'
        //echo "the new version is ${NEW_VERSION}"
      }
    }
    
    stage("test") {
      when{
        expression{
          params.executeTests
        }
      }
      steps {
        echo 'testing the application ...'
      }
    }

    stage("deploy") {
    
      steps {
        echo 'deploying the application ...'
        echo "deploying with ${params.VERSION}"
        //echo "deploying with ${SEVER_CRDENTIALS}"
        //sh "${SEVER_CRDENTIALS}"
        /*withcredentials([
          usernamePassword(credentials: 'server-credentials', usernameVariable: USER, passwordVariable: PWD)
        ]){
            sh "some script ${USER} ${PWD}"
        }
      }*/
    }
  }
  //post {
    //always {

    //}
    //success {

    //}
    //failure {

    //}
  //}
}
