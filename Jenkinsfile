pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        dir(path: '/home/shiyanlou/Code') {
          git(url: 'git@github.com:redkins/test_git.git', branch: 'main', credentialsId: '78bf7cee-01f9-4d71-9e13-f5302d68c02c')
        }

      }
    }

    stage('build') {
      steps {
        sh 'pip3 install -r requirements.txt'
      }
    }

    stage('run') {
      steps {
        sh 'python3 app.py'
      }
    }

  }
}