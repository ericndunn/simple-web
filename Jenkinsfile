pipeline {
agent { label 'MASTER' }
parameters {
// choice(choices: ['inventory', 'inventorypm'], description: '', name: 'INV_FILE')
// choice(choices: ['all', 'DEV', 'SIT', 'UATSEC', 'PERF', 'PREPROD', 'PROD', 'PRODA', 'PRODB'], description: '', name: 'INV_GRP')
}
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
