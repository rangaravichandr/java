pipeline {
    agent{
     node{
        label "java_slave"
     }
    }
    environment {
        PATH = "/usr/share/maven/bin:$PATH"
    }
    stages{
        stage("build code"){
            steps{
                sh 'mvn clean install'
            }
            
        }
    }
}
