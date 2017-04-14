node {
     pipelineTriggers( 
                      [ [   $class: 'hudson.triggers.TimerTrigger',  spec  : "*/5 * * * *"  ] ]                    
     ) 

    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev'
    echo 'Hello World'
    }
