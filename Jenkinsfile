pipeline {
    agent any

  parameters {
      string(name: 'name', defaultValue: '', description: '')
  }

  stages {
    stage("clone the repository with branch") {
      steps {
        dir("here") {
          git (
            url: "https://github.com/qiaohao9/dotfiles.git",
            branch: "master",
            changelog: true,
            poll: true
          )

          sh 'pwd'
          sh 'ls -la'
        }

        sh 'pwd'
        sh 'echo $WORKSPACE'
        sh 'ls -la'
      }
    }

    stage("print git hash") {
      steps {
        echo "${env.GIT_COMMIT}"
        echo "${params.name}"
        sh 'echo "git commit hash: $GIT_COMMIT"'
        sh 'echo "parameters ${name}"'
      }
    }
  }
}
