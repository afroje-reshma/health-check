


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

   
    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev-Env'
    echo 'Hello World '
    stage 'QA-Test'
    echo 'Hello World'
    }
        catch (err) {
      currentBuild.result = "FAILURE"
       mail body: "project build error is here: ${env.BUILD_URL}" ,
            /*from: 'afroje.reshma@gmail.com',
            replyTo: 'afrojareshma@yahoo.com',*/
            subject: 'project build failed',
            to: 'afroje.reshma@gmail.com' 
       throw err
    }
 
}

  
 

     
