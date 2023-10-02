pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the GitHub repository
                checkout scm
            }
        }

        stage('Build and Run') {
            steps {
                // Define the Python version you want to use (optional)
                def pythonVersion = '3.7' // Change this to your desired Python version

                // Set up a virtual environment
                sh """
                    python${pythonVersion} -m venv venv
                    source venv/bin/activate
                """

                // Install any necessary dependencies (if you have a requirements.txt file)
                sh "pip install -r requirements.txt"

                // Run the Python script
                sh "python hello.py"
            }
        }
    }

    post {
        always {
            // Clean up the virtual environment
            sh "deactivate"
        }
    }
}
