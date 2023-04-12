pipeline {
    agent any

    stages {
        stage("print git hash") {
            steps {
                sh 'echo "$GIT_COMMIT"'
            }
        }
    }
}
