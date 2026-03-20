pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo "Cloning repository"
                git 'https://github.com/Riddhi0179/sem-10'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo "Installing dependencies"
                sh 'pip3 install --user -r requirements.txt'
            }
        }

        stage('Run Application') {
            steps {
                echo "Running Flask App"
                sh 'pkill -f app.py || true'
                sh 'nohup python3 app.py > output.log 2>&1 &'
            }
        }
    }
}
