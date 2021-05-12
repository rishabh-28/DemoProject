pipeline {
    agent any
    stages {
        stage('git'){
            steps {
                sh 'git pull https://github.com/rishabh-28/DemoProject.git'
            }
        }
        stage('build docker image'){
            steps {
                sh 'docker build -t nodejs .'
            }
        }

        stage('Run Docker Container'){
            steps {
                sh 'docker run -itd -p 51005:51005 nodejs'
            }
        }


    }
}

