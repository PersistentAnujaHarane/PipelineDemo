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
        withDockerRegistry(credentialsId: 'docker', url: 'https://registry-1.docker.io/v2/') {
       sh "docker login -u anujaharane -p Anizhe7433  https://registry-1.docker.io/v2/ "
      sh "docker build . -t anujaharane/test:"+${env.BUILD_NUMBER}
      sh "docker push anujaharane/test"
        }

  }}
}
}
