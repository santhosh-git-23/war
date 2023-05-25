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
          deploy adapters: [tomcat9(credentialsId: 'tomcat', path: '', url: 'http://13.51.177.227:8080/')], contextPath: '/', onFailure: false, war: 'springboot-war-demo-0.0.1-SNAPSHOT.war' 
        }
      }
    }
  }
}
