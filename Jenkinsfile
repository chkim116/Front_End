pipeline {
  agent none
  stages {
    stage('Source') {
      steps {
        git(url: 'https://github.com/CafeReview/Front_End.git', branch: 'main', credentialsId: 'cafereview')
      }
    }

    stage('Build') {
      steps {
        sh 'cd mycafe && npm install && npm run build'
      }
    }

    stage('Deploy') {
      steps {
        sh 'echo "Deploy success"'
      }
    }

  }
}