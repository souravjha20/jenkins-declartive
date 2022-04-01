pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build the job'
                sh '''#!/bin/bash
                # Add two numeric value
                ((sum=25+35))
                ((sum=30+20))
                #Print the result
                echo $sum'''
            }
        }
        stage('Test') {
            steps {
                echo 'Test the job'
                echo "hello this is multibranch jenkins" 
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
