#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'node'
            args '-u root'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'cd client'
                sh 'npm install'
            }
        }
        stage('Start') {
            steps {
                echo 'Starting...'
                sh 'npm start'
            }
        }
    }
}
