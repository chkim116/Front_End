pipeline {
  agent any
  tools {nodejs "nodejs"}
  
  stages {
    stage('Source') {
      agent any
      steps {
        git(url: 'https://github.com/CafeReview/Front_End.git', branch: 'main', credentialsId: 'cafereview')
      }
    }

    stage('Build') {
      agent any
      steps {
        sh 'cd mycafe && npm install && npm run build'
      }
    }

    stage('Deploy') {
      agent any
      steps {
        sh 'echo "Deploy success"'
      }
    }

  }
}
