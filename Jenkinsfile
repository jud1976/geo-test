pipeline{
    agent any
    tools{
        maven 'M2_HOME'
    }
    stages{
        stage('maven clean'){
            steps{
             sh  'mvn clean'
            }
        }
        stage('maven install'){
            steps{
             sh   'mvn install'
            }
        }
         stage('maven package'){
            steps{
               sh 'mvn package'
            }
        }
        stage('upload artifact'){
            steps{
                nexusArtifactUploader artifacts: [[artifactId: 'bioMedical',
                 classifier: '', file: 'target/bioMedical-0.0.2-SNAPSHOT.jar',
                  type: 'jar']], credentialsId: 'NexusID', groupId: 'qa',
                   nexusUrl: 'ec2-44-203-35-83.compute-1.amazonaws.com:8080',
                    nexusVersion: 'nexus3', protocol: 'http', repository: 'Judex', version: '0.0.2-SNAPSHOT'
            }
        }
    }
}
    


