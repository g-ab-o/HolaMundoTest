pipeline {
    agent any
    tools {
        maven 'm3'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Run') {
            steps {
                sh 'java -cp target/holamundo-1.0-SNAPSHOT.jar com.holamundo.Main'
            }
        }
    }
}