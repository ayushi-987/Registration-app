pipeline{
    agent{label 'Jenkins-Agent'}
    tools{
        jdk 'Java17'
        maven 'maven3'
    }
    stages{
        stage("Checkout from SCM"){
            steps{
                cleanWs()
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/ayushi-987/Registration-app.git'
            }
        }
        stage("Build Application"){
            steps{
                sh "mvn clean package"
            }
        }
    stage("Test Application"){
        steps{
            sh "mvn test"
        }
    }
}
}