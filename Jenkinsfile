pipeline {
    agent {node 'master'}
    stages {
        stage('env') {
            steps {
                sh 'printenv'
            }
        }
        stage('Develop') {
            when {
                expression {
                    env.GIT_BRANCH == 'origin/A'
                }
            }
            steps {
                echo "Hello World at the top!"
            }
        }
        stage('Test') {
            when {
                expression {
                    env.GIT_BRANCH == 'origin/master'
                }
            } 
            steps {
                echo "Hello World at the top!??"
            }
        }
        stage('Disabled Polling') {
            when {
                expression {
                    env.GIT_BRANCH == 'origin/A'
                }
            } 
            steps {
                echo "Hello World at the top??????????"
            }
        }
    }
}