 

node {
    
  
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
    
    notify('Started')
    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev-Env'
    echo 'Hello World '
    stage 'QA-Test'
    echo 'Hello World'
  
}
  
 /* def notify(status){
      emailext (
        to: afrojareshma@yahoo.com",
        subject: "${status}: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'", */

     def notify(status){
     emailext (
      to: "afroje.reshma@gmail.com",
      subject: "${status}: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
 
      body: """<p>${status}: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]':</p>
        <p>Check console output at <a href='${env.BUILD_URL}'>${env.JOB_NAME} [${env.BUILD_NUMBER}]</a></p>""",
    )
   }
