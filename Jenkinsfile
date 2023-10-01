pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
        retry(count: 3) {
          echo 'Trying to build'
        }

      }
    }

    stage('Test1') {
      parallel {
        stage('Test1') {
          steps {
            echo 'Test1 completed'
          }
        }

        stage('Test2') {
          steps {
            echo 'Test2 completed'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you sure to deploy?', ok: 'Yes, Proceed please')
        echo 'Deployment process has been completed successfully!'
      }
    }

  }
}