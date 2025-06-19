pipeline {
    agent any
    

        stage('Preparation') {
            steps {
                echo "🛠️ Setting up environment..."
                sh '''
                    chmod +x touch.sh
                    ls -la touch.sh
                '''
            }
        }

        stage('Execute Script') {
            steps {
                echo "🚀 Executing touch.sh script..."
                sh '''
                    echo "Running touch.sh script..."
                    ./touch.sh || {
                        echo "Script execution failed"
                        exit 1
                    }
                '''
            }
        }
    }
}
