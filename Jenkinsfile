 

node {
    
    currentBuild.result = "SUCCESS"
 try {
    properties([
        [
           $class: 'BuildDiscarderProperty',
            strategy: [
               $class: 'LogRotator', 
               numToKeepStr: '5']
        ],
      pipelineTriggers([
          cron('H/30 2 * * *')
         ])
       ])
     /* pipelineTriggers([
        [$class: "SCMTrigger", scmpoll_spec: "H/5 * * * *"]
    ])*/
    
 
    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev-Env'
    echo 'Hello World '
    stage 'QA-Test'
    echo 'Hello World'
  
  
   mail body: "project build successful: ${env.BUILD_URL}",
    subject: 'project build successful',
    to: 'afrojareshma@yahoo.com'
  }
  
}
  
 

     
