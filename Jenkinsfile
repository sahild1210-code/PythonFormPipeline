pipeline {
    agent any

    stages {

        stage('Setup Python Environment') {
            steps {
                powershell 'python --version'
                powershell 'python -m pip install -r requirements.txt'
            }
        }

        stage('Run Flask App Test') {
            steps {
                powershell 'python -c "import flask; print(flask.__version__)"'
            }
        }

        stage('Build Success') {
            steps {
                echo 'Flask Jenkins pipeline executed successfully!'
            }
        }
    }
}
