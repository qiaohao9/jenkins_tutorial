pipeline {
    agent any

    parameters {
        string(name: 'name', defaultValue: '', description: 'name')
    }

    stages {
        stage("print git hash") {
            steps {
                sh 'echo "git commit hash: $GIT_COMMIT"'
                sh 'echo "parameters ${params.name}"'
            }
        }
    }
}
