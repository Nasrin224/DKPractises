node {
   
   stage('checkout') { // for display purposes
      checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '12709cc0-c778-47dd-bba4-0553f9e663b2', url: 'https://github.com/Nasrin224/DKPractises.git']]])

   }
   stage('preparation'){ //preparation
       git credentialsId: '12709cc0-c778-47dd-bba4-0553f9e663b2', url: 'https://github.com/Nasrin224/DKPractises.git'

   }
   stage('Build') {
       sh 'mvn clean compile'
       echo 'build is done'
      
   }
   stage('test'){ //testing
       sh 'mvn test'
       echo 'testing is done'
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
   

