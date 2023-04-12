pipeline {
    agent any

    parameters {
        string(name: 'name', defaultValue: '', description: '')
    }

    stages {
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
