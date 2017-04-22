
node {
  
    properties([
        [
           $class: 'BuildDiscarderProperty',
            strategy: [
               $class: 'LogRotator', 
               numToKeepStr: '10']
        ],
      pipelineTriggers([
          cron('* * * * *')
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
  
 /* def notify(status){
      emailext (
        to: afrojareshma@yahoo.com",
        subject: "${status}: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'", */

    }
