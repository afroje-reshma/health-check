


node {
    
    try {
    properties([
        [
           $class: 'BuildDiscarderProperty',
            strategy: [
               $class: 'LogRotator', 
               numToKeepStr: '5']
        ],
      pipelineTriggers([
          cron('H/30 1 * * *')
         ])
       ])
     /* pipelineTriggers([
        [$class: "SCMTrigger", scmpoll_spec: "H/5 * * * *"]
    ])*/

    stage ''
    /*stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev-Env'
    echo 'Hello World '
    stage 'QA-Test'
    echo 'Hello World'*/
    }
  finally {
        step([$class: 'Mailer', notifyEveryUnstableBuild: true, recipients: 'afrojareshma@yahoo.com', sendToIndividuals: true])
    }
 
}

  
 

     
