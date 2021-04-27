pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        dir(path: '/home/shiyanlou/Code') {
          git(url: 'git@github.com:redkins/test_git.git', branch: 'main', credentialsId: 'f16420fc-050a-4d59-94ff-98a446de6eb5')
        }

      }
    }

    stage('build') {
      steps {
        sh 'pip2 install -r requirements.txt'
      }
    }

    stage('run') {
      steps {
        sh 'python app.py'
      }
    }

  }
}