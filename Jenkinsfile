
node {
  
    properties([
        [
           $class: 'BuildDiscarderProperty',
            strategy: [
               $class: 'LogRotator', 
               numToKeepStr: '10']
        ]
     /* pipelineTriggers([
          cron('* 8 * * *')
         ])*/
       ])
     /* pipelineTriggers([
        [$class: "SCMTrigger", scmpoll_spec: "H/5 * * * *"]
    ])*/
    
   


    stage 'Checkout-Code'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev-Env'
    echo 'Hello Beautiful World '
    stage 'QA-Test'
    echo 'Hello World'
    }
