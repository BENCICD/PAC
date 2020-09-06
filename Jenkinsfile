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
                echo "Hello Dev"
            }
        }
        stage('Test') {
            when {
                expression {
                    env.GIT_BRANCH == 'origin/master'
                }
            } 
            steps {
                echo "Hello Test"
            }
        }
        stage('Disabled Polling') {
            when {
                expression {
                    env.GIT_BRANCH == 'origin/A'
                }
            } 
            steps {
                echo "Hello Poll"
            }
        }
    }
}