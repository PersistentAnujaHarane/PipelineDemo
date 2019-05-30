
pipeline {
  agent { dockerfile true }
    
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
     
stage('Docker Build'){
    steps{
        {tools docker "Docker"}
      sh "docker build . -t anujaharane/test:"+${env.BUILD_NUMBER}
      sh "docker push anujaharane/test"
  }}
}
}
