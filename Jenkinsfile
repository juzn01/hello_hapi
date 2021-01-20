#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'node'
            args '-u 1000'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'chmod 777 package-lock.json'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'npm test'
            }
        }
    }
}
