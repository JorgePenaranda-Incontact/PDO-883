pipeline {
  agent any

  stages {
    stage('Check Containers') {
      input {
        message "If Bitbucket containers are already running or stoped they will be removed, Should we remove them?"
        ok "Yes, remove the containers"
      }
      steps {
        //script {
          //def gs = load("groovy_scripts/groovy_functions.groovy")
          //gs.check_containers()
        //}
        dir("scripts"){
          sh 'chmod +x containers-check.sh'
          sh './containers-check.sh'
        }
      }
    }
  }
}