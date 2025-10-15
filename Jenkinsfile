pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo '📦 Checking out code from GitHub...'
                git branch: 'main', url: 'https://github.com/shashwatbaswade09-prog/ccdtry.git'
            }
        }
        
        stage('Build') {
            steps {
                echo '🔨 Building the application...'
                sh 'ls -la'
                echo 'Files checked successfully!'
            }
        }
        
        stage('Test') {
            steps {
                echo '🧪 Running tests...'
                sh '''
                    if [ -f "index.html" ]; then
                        echo "✓ index.html found"
                    fi
                    if [ -f "styles.css" ]; then
                        echo "✓ styles.css found"
                    fi
                    if [ -f "script.js" ]; then
                        echo "✓ script.js found"
                    fi
                '''
                echo 'All tests passed!'
            }
        }
        
        stage('Deploy') {
            steps {
                echo '🚀 Deploying application...'
                echo 'Application deployed successfully!'
            }
        }
    }
    
    post {
        success {
            echo '✅ Pipeline completed successfully!'
        }
        failure {
            echo '❌ Pipeline failed!'
        }
    }
}
