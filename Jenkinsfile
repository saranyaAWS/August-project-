pipeline{
    agent any

    stages{
       stage('git clone'){
        steps{
            git credentialsId: 'github_creds', url: 'https://github.com/saranyaAWS/August-project-.git'
        }
       }
       stage('build'){
        steps{
            sh 'mvn clean package'
        }
       }
      stage('test'){
        steps{
            sh 'mvn --version'
        }
      }
      stage('deploy'){
        steps{
            'java -jar target/Java-1.0-SNAPSHOT.jar'
        }
      }
    }


}
