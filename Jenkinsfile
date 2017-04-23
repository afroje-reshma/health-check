 

node {
    
    currentBuild.result = "SUCCESS"
    properties([
        [
           $class: 'BuildDiscarderProperty',
            strategy: [
               $class: 'LogRotator', 
               numToKeepStr: '5']
        ],
      pipelineTriggers([
          cron('* * * * *')
         ])
       ])
     /* pipelineTriggers([
        [$class: "SCMTrigger", scmpoll_spec: "H/5 * * * *"]
    ])*/
    
 try {
    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev-Env'
    echo 'Hello World '
    stage 'QA-Test'
    echo 'Hello World'
  
  
   mail body: 'project build successful'
    from: 'afroje.reshma@gmail.com',
    replyTo: 'xxxx@yyyy.com',
    subject: 'project build successful',
    to: 'afrojareshma@yahoo.com'
  }
  
}
  
 

     
