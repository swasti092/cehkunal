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
      }
    }
     
    stage ('Source Composition Analysis') {
      steps {
         
         sh 'wget "https://raw.githubusercontent.com/cehkunal/webapp/master/owasp-dependency-check.sh" '
         echo "PATH =Swasti 4"
         sh 'chmod +x owasp-dependency-check.sh'
         echo "PATH =Swasti 5"
         /*sh 'bash owasp-dependency-check.sh'*/
         echo "WORKSPACE = ${WORKSPACE}"
       /* sh 'bash /var/jenkins_home/dependency-check/bin/dependency-check.sh --purge'*/
         sh 'bash /var/jenkins_home/dependency-check/bin/dependency-check.sh --scan ${WORKSPACE}/src -f xml -o ${WORKSPACE}/ --project "owasp-dependency-check" '
         sh 'cat ${WORKSPACE}/dependency-check-report.xml.xml'
        
      }
    }
    
 
    
   /* stage ('Build') {
      steps {
      sh 'mvn clean package'
       }
    }*/

    
  }
}
