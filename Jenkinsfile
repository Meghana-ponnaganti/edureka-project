pipeline {
    agent any
    environment {
        //be sure to replace "bhavukm" with your own Docker Hub username
        DOCKER_IMAGE_NAME = "bhavukm/train-schedule"
    }
    stages {
        stage('puppet agent') {
            steps {
                echo 'Running build automation'
               
            }
        }
        stage('puppet certificate') {
            when {
                branch 'master'
            }
            steps {
                script {
                    app = docker.build(DOCKER_IMAGE_NAME)
                    app.inside {
                        sh 'echo Hello, World!'
                    }
                }
            }
        }
        stage('trigger puppet') {
            when {
                branch 'master'
            }
            steps {
                script {
                    //docker.withRegistry('https://registry.hub.docker.com', 'docker_hub_login') {
                        //app.push("${env.BUILD_NUMBER}")
                        //app.push("latest") 
                   // } 
                    sh 'echo Hello, World!'
                } 
                
            } 
        }
        stage('Deploy') {
            when {
                branch 'master'
            }
            environment { 
                CANARY_REPLICAS = 1
            }
            steps {
                 //kubernetesDeploy(
                    //kubeconfigId: 'kubeconfig',
                    //configs: 'train-schedule-kube-canary.yml',
                    //enableConfigSubstitution: true
              //  )
                sh 'echo Hello, World!'
            }
        }
    }
}
