pipeline {
    agent any
    stages {
        stage ("Code Clone"){
            steps{
                git url:"https://github.com/priya2044/Watch-Website.git", branch: "main"
            }
        }
        stage ("Code Build"){
            steps{
                echo "Building the image"
                sh "docker build -t my-app ."
            }
        }
        stage ("Code Deployed"){
            steps{
                echo "Deploying the container"
                sh "docker-compose down && docker-compose up -d"
            }
        }
    }
}
