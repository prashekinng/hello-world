node{
   stage('git checkout'){
       git 'https://github.com/prashekinng/hello-world'
   }
   
   stage('compile and package'){
       //get maven home path
       def mvnHome = tool name: 'maven', type: 'maven'
       sh "${mvnHome}/bin/mvn package
   }
 }  
