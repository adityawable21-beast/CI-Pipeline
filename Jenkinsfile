pipeline{
    agent any
    stages{
        stage('Setup'){
            steps{
                echo 'Installing dependencies...'
                bat '"C:\\Users\\adity\\AppData\\Local\\Microsoft\\WindowsApps\\python.exe" -m pip install -r requirements.txt'
            }
        }
        stage('Build & Test'){
            steps{
                echo 'Running ML pipeline'
                bat '"C:\\Users\\adity\\AppData\\Local\\Microsoft\\WindowsApps\\python.exe" ml_pipeline.py'
            }
        }

    }
    post{
        success{
            echo 'Pipeline SUCCESS - Model validated'
        }
        failure{
            echo 'Pipeline FAIL'
        }
    }
}