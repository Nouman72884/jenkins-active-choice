pipeline {
  agent any
  parameters {
    choice(choices: ['FRONT-END', 'BACK-END'], name: 'DEPLOYMENT_END', description: 'please choose the environment you want to deploy?')
  }
  stages {
    stage ('Clone') {
        steps {
            git branch: params.Branches , url: "${GIT_URL}"
        }
    }
    stage('FRONT-END Deployment') {
    // when {
    // expression {
    //         return params.DEPLOYMENT_END == 'FRONT-END' && params.Branches == 'master';
    //     }
    // }
      steps {
        script {
          sh 'echo FRONT-END'
          sh 'ls'
          sh 'cat master-branch.txt'
        }
      }
    }
    stage('BACK-END Deployment') {
    // when {
    // expression {
    //         return params.DEPLOYMENT_END == 'BACK-END' && params.Branches == 'dev';
    //     }
    // }
      steps {
        script {
          sh 'echo BACK-END'
          sh 'ls'
          sh 'cat master-branch.txt'
        }
      }
    }
  }
}