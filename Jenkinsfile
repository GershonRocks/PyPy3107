pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                git 'https://github.com/LiorRocks/PyPy3107.git'
                sh 'hello.py'
            }
        }
    }
}
