
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
    [
        $class: 'GithubProjectProperty',
        displayName: '',
        projectUrlStr: 'https://github.com/xxxxxxx/xxxxx-xxxx/'
      ]
    ])
    
    stage 'Checkout'   
    checkout scm
    def project_path = "health-check"
    stage 'Dev'
    echo 'Hello World'
    }
