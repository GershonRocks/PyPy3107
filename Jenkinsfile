pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                sh '''#!/bin/bash
                cd PyPy3107
                python3 hello.py'''
            }
        }
    }
}
