
node {
  
    properties([
        [
           $class: 'BuildDiscarderProperty',
            strategy: [
               $class: 'LogRotator', 
               numToKeepStr: '10']
        ],
        /*pipelineTriggers([
          cron('H/30 8 * * *')
        ])*/
      pipelineTriggers([
        [$class: "SCMTrigger", scmpoll_spec: "* * * * *"],
    ])
    ])


    stage 'Checkout-code'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev'
    echo 'Hello World'
    }
