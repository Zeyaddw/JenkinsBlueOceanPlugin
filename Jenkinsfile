pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
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
        echo 'Deployment process has been completed successfully!'
      }
    }

  }
}