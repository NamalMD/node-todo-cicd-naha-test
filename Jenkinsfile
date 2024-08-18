pipeline {
    agent { label 'dev' }
     

    stages {

        stage ('Code') {
            steps {
                git url: 'https://github.com/ajitfawade/node-todo-cicd.git', branch: 'master'
                echo ' pull from master '
            }
        }
        
        stage ('Build & Test') {
            steps {
                echo 'Build & Test'
                sh 'docker build . -t ajitfawade14/node-todo-app:latest'
            }
        }

        stage ('Deploy') {
            steps {
                echo 'Deploying'
                echo 'done by me - new 3'
                sh 'docker run ajitfawade14/node-todo-app:latest -p 8000:8000 --name new-app'
            }
        }

    }
}
