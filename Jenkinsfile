
node {
     properties (
     pipelineTriggers( 
                      [
                           [  
                                $class: 'hudson.triggers.TimerTrigger',  
                                spec  : '* * * * *' 
                           ] 
                      ] 
          )
        )  
    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
       stage 'Dev'
    echo 'Hello World'
    }
