


node {
    
    //currentBuild.result = "SUCCESS"
    try {
    /*properties([
        [
           $class: 'BuildDiscarderProperty',
            strategy: [
               $class: 'LogRotator', 
               numToKeepStr: '5']
        ],
      pipelineTriggers([
          cron('H/59 4 * * *')
         ])
       ])*/
     /* pipelineTriggers([
        [$class: "SCMTrigger", scmpoll_spec: "H/5 * * * *"]
    ])*/

   
    stage 'Check'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev-Test-Trigger'
    echo 'Hello Beautiful World '
    stage 'QA-Test-Trigger'
    echo 'Hello Handsome'
     
        //mail body: "project build successful is here: ${env.BUILD_URL}" ,
            /*from: 'afroje.reshma@gmail.com',
            replyTo: 'afrojareshma@yahoo.com',*/
        //  subject: 'project build is successful hee hee haa haa',
        //  to: 'afrojareshma@yahoo.com'    
        
        
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

  
 

     
