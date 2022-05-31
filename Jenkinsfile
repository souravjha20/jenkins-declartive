pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build the job'
                sh '''#!/bin/bash
                # Add two numeric value
                ((sum=75+55))
                ((sum=30+80))
                #Print the result
                echo $sum'''
            }
        }
        stage('Test') {
            steps {
                echo 'Test the job'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy the job'
                git branch: 'main', url: 'https://github.com/souravjha20/jenkins-pipeline.git'
            }
        }
        stage('Release') {
            steps {
                echo 'Release the job'
            }
        }    
    }
}
