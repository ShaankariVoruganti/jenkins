pipeline{
  agent any
  stages{
    stage('git clone'){
      steps{
        sh 'https://github.com/ShaankariVoruganti/jenkins'
      }
    }
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
  }
}
