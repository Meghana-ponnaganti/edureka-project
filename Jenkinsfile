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
           
            steps {
                script {
                    //app = docker.build(DOCKER_IMAGE_NAME)
                    //app.inside {
                        sh 'echo Hello, World!'
                    }
                }
            }
        }
        stage('trigger puppet') {
            
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
