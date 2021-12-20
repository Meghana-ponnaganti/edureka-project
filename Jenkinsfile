pipeline {
    agent any

    stages {
        stage('puppet config') {
            steps {
                echo 'Running build automation'
                //sh './gradlew build --no-daemon'
                //archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
        stage('puppet certificate') {
            
            steps {
                script {
                    //app = docker.build(DOCKER_IMAGE_NAME)
                    //app.inside {
                        sh 'echo Hello, World!'
                    //}
                }
            }
        }
        stage('Puppet trigger') {
        
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
                sh './gradlew build --no-daemon
                sh 'echo Hello, World!'
            }
        }
        
    }
}
