node {
   
   stage('checkout') { // for display purposes
      checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '78bf7588-0e63-4171-bdf0-673910b6e365', url: 'https://github.com/Nasrin224/DKPractises.git']]])
   }
   stage('preparation'){ //preparation
       git credentialsId: '78bf7588-0e63-4171-bdf0-673910b6e365', url: 'https://github.com/Nasrin224/DKPractises.git'

   }
   stage('Build') { //building
      withMaven(jdk: 'java 1.8.0_151', maven: 'maven 3.5.2') {
    sh 'mvn clean compile'
       echo 'build is done'
   }
     
   }
   stage('test'){ //testing
      withMaven(jdk: 'java 1.8.0_151', maven: 'maven 3.5.2') {
       sh 'mvn test'
       echo 'testing is done'
      }
   }
   stage('Results') {
       echo 'results are generated'
      
   }
   
   stage('Archive') {
       echo 'Archived Test Reports'
   
   }
   stage('Deploy') {
       echo 'Deployed the artifacts'
     
   }
}
   

