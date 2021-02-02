pipeline {
  agent {
    node {
      label 'cafereview01'
    }

  }
  stages {
    stage('Source') {
      agent {
        node {
          label 'cafereview01'
        }

      }
      steps {
        git(url: 'https://github.com/CafeReview/Front_End.git', branch: 'main', credentialsId: 'cafereview')
      }
    }

    stage('Build') {
      agent {
        node {
          label 'cafereview01'
        }

      }
      steps {
        sh 'cd mycafe && npm install && npm run build'
      }
    }

    stage('Deploy') {
      agent {
        node {
          label 'cafereview01'
        }

      }
      steps {
        sh 'echo "Deploy success"'
      }
    }

  }
}