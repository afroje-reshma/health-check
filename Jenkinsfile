
node {
   properties([
    pipelineTriggers([
        cron('H/30 8 * * *')
    ])
])
    
    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev'
    echo 'Hello World'
    }
