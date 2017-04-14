node {
    pipelineTriggers( 
     [ 
    [ 
        $class: 'hudson.triggers.TimerTrigger', 
        spec  : "*/1 * * * *" 
        ] 
         ] 
       )     

   stage 'Dev'
   echo 'Hello World'
   stage 'Test'
   echo 'Hello World'
   stage 'Production'
   echo 'Hello World'
   }
