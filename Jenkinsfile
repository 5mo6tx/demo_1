import groovy.sql.Sql

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
                   // bat 'mysql -u root -p'
                      def sql = Sql.newInstance("ec2-13-58-23-69.us-east-2.compute.amazonaws.com:3306/inventory", "root","debezium", "com.mysql.jdbc.Driver")
                      def rows = sql.execute "select count(*) from test1;"
                      echo rows.dump()
                 }     
            }
        }
       
        
    }
}
        
  


