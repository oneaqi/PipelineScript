pipeline {
   agent any

   tools {
   
      maven "Maven_Centos"
   }

   stages {
      stage('SCM') {
         steps {
            // Get some code from a GitHub repository
            git credentialsId: 'd1096f94-70cb-4942-ac85-443fae9bef54', url: 'https://github.com/oneaqi/Javaweb_nexus.git'
                 
        }

      }
    stage('Build'){
        steps{
            // Run Maven on a Unix agent.
            sh "mvn -Dmaven.test.failure.ignore=true clean package"        
        }
    }    
    
//    stage('Deploy'){
//        steps{
//deploy adapters: [tomcat7(credentialsId: 'dd868150-787c-4767-a317-d7a51651f19e', path: '', url: 'http://192.168.56.103:8082/')], contextPath: 'NexusJob', war: '**/*.war'    }
//   }
   
}
}
