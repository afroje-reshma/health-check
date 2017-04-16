
node {
   properties([
    pipelineTriggers([
        cron('* * * * *')
    ])
])
    
    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev'
    echo 'Hello World'
    }
