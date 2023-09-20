node {

  stage('Checkout') {
    steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/feature-ms-TeddyAlfaro-mensaje']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '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', url: 'https://github.com/DevOps-Fundamentos-v4/microservicio-spring.git']]])
    }
  }

  stage('Build'){
    checkout scm
    sh "chmod 777 gradlew"
     sh "./gradlew build"
  }
  
  stage('Test'){
  sh "./gradlew clean test"
  }

  stage('Deploy') {
    steps {
        echo 'Deploying....'
    }
  }

}
