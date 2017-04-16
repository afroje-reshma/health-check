
node {
    properties([
    pipelineTriggers([
        scm('* * * * *')
    ])
])
    
    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev'
    echo 'Hello World'
    }
