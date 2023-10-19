pipeline {
    agent any
    stages {

        stage("Build")
        {
            steps
            {
                script {
                        echo "INFO: Build Stage"
                        sh "docker build -t nodejs-demo:latest ."
                        echo "INFO: Docker Image Built"
                    }
            }
        }

        stage("Deploy")
        {
            steps
            {
                script {
                            echo "INFO: Running New Docker Image"
                            sh "docker rm -f nodejs-demo || true"
                            sh "docker run --restart always -p 3000:3000 -d --name nodejs-demo nodejs-demo:latest"
                            echo "INFO: Docker Deployed"
                    }
            }
        }
    }
}
