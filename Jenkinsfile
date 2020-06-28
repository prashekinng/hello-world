node{
   stage('git checkout'){
       git 'https://github.com/prashekinng/hello-world'
   }
   
   stage('compile and package'){
       //get maven home path
       def mvnHome = tool name: 'maven', type: 'maven'
       sh "${mvnHome}/bin/mvn package"
   }
   
   stage('Email Notifications'){
       mail bcc: '', body: '''haai prashe! welcome to email notifications of jenkins.
       thanks, prashe.''', cc: '', from: '', replyTo: '', subject: 'jenkins job details  notifications', to: 'prashanth.bura6465@gmail.com'
   }
 }  
