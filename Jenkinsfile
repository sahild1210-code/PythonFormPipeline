pipeline {
    agent any

    stages {

        stage('Setup Python Environment') {
            steps {
                bat 'python --version'
                bat 'python -m pip install -r requirements.txt'
            }
        }

        stage('Run Flask App Test') {
            steps {
                bat 'python -c "import flask; print(flask.__version__)"'
            }
        }

        stage('Build Success') {
            steps {
                echo 'Flask application build successful!'
            }
        }
    }
}
