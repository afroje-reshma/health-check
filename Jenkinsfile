
node {
  
    properties([
        [
           $class: 'BuildDiscarderProperty',
            strategy: [
               $class: 'LogRotator', 
               numToKeepStr: '10']
        ],
      pipelineTriggers([
          cron('H/10 10 * * *')
         ])
       ])
     /* pipelineTriggers([
        [$class: "SCMTrigger", scmpoll_spec: "H/5 * * * *"]
    ])*/
    
   


    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev-Env'
    echo 'Hello Beautiful World '
    stage 'QA-Test'
    echo 'Hello World'
    }
