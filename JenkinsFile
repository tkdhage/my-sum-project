pipeline {
    agent any 

    parameters {
        string(name: 'NUM1', defaultValue: '5', description: 'Enter first number')
        string(name: 'NUM2', defaultValue: '10', description: 'Enter second number')
    }

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Compile and Run Java Program') {
            steps {
                sh "javac SumCalculator.java"
                sh "java SumCalculator ${params.NUM1} ${params.NUM2}"
            }
        }
    }
}
