pipeline{
  tools{
    maven 'Maven'
  }
  stages{
    stage('Checkout'){
      steps{
        git branch:'main',url:'https://github.com/chinmayiii/2026simplemaven.git'
      }
    }
    stage('Build'){
      steps{
        sh 'mvn clean package'
      }
    }
    stage('Test'){
      steps{
        sh 'mvn test'
      }
    }
    stage('Run Application'){
      steps{
        sh 'mvn run'
      }
    }
  }
    post{
      success{
        echo 'Build and Deployment successfull'
      }
      failure{
        echo 'Build failed'
      }
    }
  }
