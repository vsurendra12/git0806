pipeline {
    agent any
    stages {
        stage("build") {
            steps {
                echo "build stage in master machine"
                sh "hostname -i"
            }
        }
        stage("sonar") {
            agent {
                label {
                    java-slave
                steps {
                    echo "this is slave machine"
                    sh "hostname -i"
                }
            }
            
        }
        
    }
    
}
}
