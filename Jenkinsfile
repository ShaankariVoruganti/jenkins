pipeline{
  agent any
  stages{
    stage(‘Checkout’) {
        steps {
         checkout([$class: ‘GitSCM’, branches: [[name: ‘*/main’]], extensions: [], userRemoteConfigs: [[url: ‘ https://github.com/ShaankariVoruganti/jenkins.git‘]]])
        }
       }
    /*stage('git clone'){
      steps{
        sh 'git clone https://github.com/ShaankariVoruganti/jenkins'
      }
    }*/
        stage('init'){
      steps{
        sh 'terraform init'
      }
    }
    stage('validate'){
      steps{
        sh 'terraform validate'
      }
    }
    stage('plan'){
      steps{
        sh 'terraform plan'
      }
    }
    stage('apply'){
      steps{
        sh 'terraform apply --auto-approve'
      }
    }
  } 
}
