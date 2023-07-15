pipeline {
  agent {
        docker {
            image 'node'
            args '-p 3000:3000'
        }
    }

  stages {
    stage('Build') {
      steps {
        sh 'npm install' // Install Node.js dependencies
      }
    }

    stage('Test') {
      steps {
        sh 'npm test' // Run tests, if any
      }
    }

    stage('Deploy') {
      steps {
        sh 'npm start' // Start the web application
      }
    }
  }
}
