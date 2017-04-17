
node {
   properties([
    pipelineTriggers([
        cron('* * * * *')
    ])
])
   
  properties([ 
      [
        $class: 'BuildDiscarderProperty',
        strategy: [
          $class: 'LogRotator',
          numToKeepStr: '10'
          ]
       ]])
    
    stage 'Checkout-code'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev'
    echo 'Hello World'
    }
