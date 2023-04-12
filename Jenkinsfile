pipeline {
    agent any

    parameters {
        string(name: 'name', defaultValue: '', description: '')
    }

    stages {
        stage("print git hash") {
            envrionment {
                name = params.name
            }
            steps {
                sh 'echo "git commit hash: $GIT_COMMIT"'
                sh 'echo "parameters ${name}"'
            }
        }
    }
}
