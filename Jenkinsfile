pipeline {
    agent any
    stages {
        stage("build") {
            steps {
                echo "running on master"
                sh "hostaname -i"
            }
        }
        stage("test"){
            agent {
                label "java-slave"
            }
            steps {
                echo "running on slave machine"
                sh "hostname -i"
            }
        }
    }
}
