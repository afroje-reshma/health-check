
node {
  
    properties([
        [
           $class: 'BuildDiscarderProperty',
            strategy: [
               $class: 'LogRotator', 
               numToKeepStr: '10']
        ],
      pipelineTriggers([
          cron('H/1 * * * *')
        ]),
      pipelineTriggers([
        [$class: "SCMTrigger", scmpoll_spec: "* * * * *"]
    ])
    ])


    stage 'Git-Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev'
    echo 'Hello World'
    stage 'QA'
    echo 'Hello World'
    }
