
pipeline {
  agent any
    tools {nodejs "Nodejs"}

  stages {
        
    stage('Cloning Git') {
      steps {
        git credentialsId: 'Git', url: 'https://github.com/PersistentAnujaHarane/JenkinsDemo.git'
       
      }
    }
        
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
     

}
}
