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
     
      
stage('Docker Build'){
    steps{
       sh "docker login -u anujaharane -p Anizhe7433  https://registry-1.docker.io/v2/ "
      sh "docker build . -t helloworld:2.0"
      sh "docker push anujaharane/test"
    

  }}
}
}
