
node {
  
    properties([
        [
           $class: 'BuildDiscarderProperty',
            strategy: [
               $class: 'LogRotator', 
               numToKeepStr: '10']
        ],
      pipelineTriggers([
          cron('* 8 * * *')
         ])
       ])
     /* pipelineTriggers([
        [$class: "SCMTrigger", scmpoll_spec: "H/5 * * * *"]
    ])*/
    
   


    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev'
    echo 'Hello World'
    stage 'QA'
    echo 'Hello World'
    }
