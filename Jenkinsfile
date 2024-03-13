pipeline {
    agent any
    tools {
    jdk 'myJava'
    maven 'myMaven'
    }
    stages {
      stage('Clonerepo') {
         steps {
            git 'https://github.com/myspace-ankit/DevOpsClassCodes.git'
         }
      }
      stage('Compile') {
         steps {
            sh 'mvn compile'
         }
      }
      stage('CodeReview') {
         steps {
            sh 'mvn pmd:pmd'
         }
      }
      stage('UnitTesting') {
         steps {
            sh 'mvn test'
         }
      }
   }
}
