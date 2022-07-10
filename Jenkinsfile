pipeline {
  agent any
  stages {
    stage('Install web server') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Fetch Code') {
      steps {
        git(url: 'https://github.com/8341828968/excler-devops.git', branch: 'main', poll: true)
      }
    }

    stage('Deploy the portal') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}