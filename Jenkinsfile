pipeline {
  agent any
  
  tools {
    maven 'Maven'
  }
  stages {
    stage ('Initialize') {
      steps {
        
        echo "PATH = ${PATH}"
       
        echo "M2_HOME = ${M2_HOME}"
       
          sh '''
        
          '''
          echo "PATH1111 = ${PATH}"
        
      }
    }
     
    stage ('Source Composition Analysis') {
      steps {
         
         sh 'wget "https://raw.githubusercontent.com/cehkunal/webapp/master/owasp-dependency-check.sh" '
         echo "PATH =Swasti 4"
         sh 'chmod +x owasp-dependency-check.sh'
         echo "PATH =Swasti 5"
         /*sh 'bash owasp-dependency-check.sh'*/
         sh 'bash /var/jenkins_home/dependency-check/bin/dependency-check.sh --help'
         //sh 'cat /var/lib/jenkins/OWASP-Dependency-Check/reports/dependency-check-report.xml'
        
      }
    }
    
 
    
    stage ('Build') {
      steps {
      sh 'mvn clean package'
       }
    }

    
  }
}
