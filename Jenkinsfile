
node {
  /* properties([
    pipelineTriggers([
        cron('H/30 8 * * *')
    ])
])*/
   
  properties([ 
      [
        $class: 'BuildDiscarderProperty',
        strategy: [
          $class: 'LogRotator',
          numToKeepStr: '10'
          ]
       ],
    ])
    
    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev'
    echo 'Hello World'
    }
