node{
   stage('git checkout'){
       git 'https://github.com/prashekinng/hello-world'
   }
   
   stage('compile and package'){
       //get maven home path
       def mvnHome = tool name: 'maven', type: 'maven'
       sh "${mvnHome}/bin/mvn package"
   }
   
   stage('Slack Notifications'){
      slackSend baseUrl: 'https://hooks.slack.com/services/', 
      channel: 'jenkins-pipeline', 
      color: 'good', 
      message: 'hey, u got a message from jenkins!', 
      teamDomain: 'cookies', 
      tokenCredentialId: 'slack-demo', 
      username: 'cookies'
   }
 }  
