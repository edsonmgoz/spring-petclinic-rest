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
        stage('Compile') {
            steps {
                sh 'mvn clean compile -B -ntp'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test -B -ntp'
                // sh 'mvn test -Dmaven.test.failure.ignore=true -B -ntp'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package -DskipTests -B -ntp'
            }
        }
    }
}