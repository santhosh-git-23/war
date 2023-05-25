pipeline {
  agent any
//   tools {
//     maven 'maven' 
//   }
//   triggers {
//     pollSCM '* * * * *'
//   }
  stages {
//     stage ('Build') {
//       steps {
//         sh 'mvn clean package'
//       }
//     }
    stage ('Deploy') {
      steps {
        script {
          deploy adapters: [tomcat9(credentialsId: 'tomcat', path: '', url: 'http://16.170.239.110:8080/')], contextPath: '/greeting', onFailure: false, war: 'greeting.war' 
        }
      }
    }
  }
}
