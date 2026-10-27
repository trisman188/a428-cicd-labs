pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building React App...'
                sh 'echo "Build success"'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "Test success"'
            }
        }

        // Kriteria 4: Stage Manual Approval
        stage('Manual Approval') {
            steps {
                input message: 'Lanjutkan ke tahap Deploy?', ok: 'Proceed'
            }
        }

        // Kriteria 2: Stage Deploy (nama stage WAJIB "Deploy")
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh 'echo "Deploying app..."'
                
                // Kriteria 3: Jeda eksekusi selama 1 menit lalu otomatis selesai
                sleep time: 1, unit: 'MINUTES'
            }
        }
    }
}
