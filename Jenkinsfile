pipeline{
  agent any
  stages{
    stage('docker build'){
      steps{
      sh 'docker build -t reactjs:v2 .'
      }
  }
  stage('docker tagging'){
    steps{
    sh 'docker tag reactjs:v1 malleshdevops/devopseks17:reactjs-v2'
    }
  }
 stage('docker login'){
   steps{
   sh 'docker login'
   }
 }
    stage('docker image push'){
      steps{
    sh 'docker push malleshdevops/devopseks17:reactjs-v2'
    }
    }
}
}
