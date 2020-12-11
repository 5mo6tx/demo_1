pipeline{
    agent any
    stages{
        stage("ECHO THINGS"){
            steps{
                
                //echo "${}"
                echo "dswncjkbwskj"
               //withKafkaLog(kafkaServers: 'ec2-13-58-23-69.us-east-2.compute.amazonaws.com:9092', kafkaTopic: 'buildlogs', metadata:'Other info to send..') {
               // echo "${env.BUILD_NUMBER}"
               // echo "${env.NODE_NAME}"
              //  echo "5mo6tx/demo"
                //echo "dcdscds"
                //echo "triggred by webhook"
            //}
            
            }
        }
        stage("testing DB"){
            steps{
                 script {
                    withCredentials([string(credentialsId: 'jenkins-database-username', variable: 'DATABASE_USERNAME')]) {
                        withCredentials([string(credentialsId: 'jenkins-database-password', variable: 'DATABASE_PASSWORD')]) {
                            def test_database_credentials = buildTestMySQLDatabase {
                                dbUser = env.DATABASE_USERNAME
                                dbPass = env.DATABASE_PASSWORD
                            }
                            echo 'Test Database Name: ' + test_database_credentials.dbName
                            echo 'Test Username: ' + test_database_credentials.testUsername
                            echo 'Test User Password: ' + test_database_credentials.testUserPassword
                        }
                      }
                 }     
            }
        }
       
        
    }
}
        
  


