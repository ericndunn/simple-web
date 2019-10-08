pipeline {
agent { label 'MASTER' }
    stages {
        stage ('Initialize') {
            steps {
                sh '''#!/bin/bash

                    echo "Hello from bash"
                    echo "Who do I $SHELL"
                '''
            }
        }

        stage ('Build') {
            steps {
                sh '/usr/local/maven/bin/mvn install' 
            }
        }
    }
}
