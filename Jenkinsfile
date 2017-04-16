
node {
     
    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    pipelineTriggers( 
                      [
                           [  
                                $class: 'hudson.triggers.TimerTrigger',  
                                spec  : "* * * * *"  
                           ] 
                      ] 
         )
    stage 'Dev'
    echo 'Hello World'
    }
