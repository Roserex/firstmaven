pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('gitintegration') {
            steps {
                echo 'Cloning git repo'
                git branch: 'main', credentialsId: 'pipegit', url: 'https://github.com/Roserex/firstmaven.git'
            }
        }
        stage('list dir') {
            steps {
                bat 'dir'
            }
        }
        stage('Build another one job') {
            steps {
                build 'linejob'
            }
        }
        stage('Wait for an input') {
            steps {
                input 'Enter your name'
            }
        }
        stage('where you are') {
            steps {
                pwd()
            }
        }
        stage('Write a file') {
            steps {
                writeFile encoding: 'Base64', file: 'C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\pipelinejob.txt', text: 'This a text file in pipeline job'
            }
        }
        
    }
}
