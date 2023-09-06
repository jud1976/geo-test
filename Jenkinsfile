pipeline{
    agent any
    stages{
        stage('mave clean'){
            steps{
                sh 'mvn clean'
            }
        }
        stage('maven install'){
            steps{
                sh 'mvn install'
            }
        }
         stage('maven package'){
            steps{
                sh 'mvn package'
            }
        }
    }
}
    


