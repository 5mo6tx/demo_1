pipeline{
    agent any
    stages{
        stage("ECHO THINGS"){
            steps{
                echo "hhhhhhhhhhhh"
            
            }
        }
        stage("kafka logs"){
            withKafkaLog(kafkaServers: 'http://ec2-3-14-142-162.us-east-2.compute.amazonaws.com:9092', kafkaTopic: 'buildlogs', metadata:'Other info to send..') {
            echo 'Hello World'
            echo 'Oh Hello'
            echo 'Finally'
         }
        
        }
    }

}
