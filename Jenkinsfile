pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo "Cloning repository"
            }
        }

        stage('Install Dependencies') {
            steps {
                echo "Installing dependencies"
                sh 'sudo apt update'
                sh 'sudo apt install -y python3-pip'
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Run Application') {
            steps {
                echo "Running Flask App"
                sh 'nohup python3 app.py &'
            }
        }

    }
}
