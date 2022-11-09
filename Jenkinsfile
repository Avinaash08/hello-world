pipeline {
  agent any
  environment {
    PATH ="/opt/maven3/bin:$PATH"
  }
  stages {
    stage('Build') {
      steps
      {
       sh "mvn clean package"
      }
    }
    stage('Deploy') {
      steps {
        sh '''
        cp webapp/target/webapp.war /opt/tomcat/webapps
        ls /opt/tomcat/webapps/
        '''
      }
    }
  }
}
