pipeline{
    agent any
    stages{
        stage("ECHO THINGS"){
            steps{
                echo "hhhhhhhhhhhh"
            
            }
        }
       
        
        }
        node {
    withKafkaLog(kafkaServers: 'host1.example.com:9092,host2.example.com:9092', kafkaTopic: 'buildlogs', metadata:'Other info to send..') {
        echo 'Hello World'
        echo 'Oh Hello'
        echo 'Finally'
    }
}
    }

}
