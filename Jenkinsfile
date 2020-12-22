pipeline {
  agent any
  parameters {
    choice(choices: ['FRONT-END', 'BACK-END'], name: 'DEPLOYMENT_END', description: 'please choose the environment you want to deploy?')
  }
  stages {
    
    stage('Pretest') {
      steps {
        script {
         
          sh 'cat master-branch.txt'
        }
      }
    }
    stage ('Clone') {
        steps {
            git branch: params.Branches , url: "${GIT_URL}"
        }
    }
    stage('FRONT-END Deployment') {
      steps {
        script {
          sh 'echo FRONT-END'
          sh 'cat master-branch.txt'
        }
      }
    }
    stage('BACK-END Deployment') {
      steps {
        script {
          sh 'echo BACK-END'
          sh 'cat master-branch.txt'
        }
      }
    }
  }
}
