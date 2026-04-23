pipeline {
    agent any
    tools {
        maven 'maven3.9.15'
    }
    stages {
        // stage('Checkout SCM') {
        //     steps {
        //         git url: 'https://github.com/edsonmgoz/spring-petclinic-rest.git'
        //     }
        // }
        stage('Build') {
            steps {
                sh 'mvn clean package -B -ntp'
            }
        }
    }
}