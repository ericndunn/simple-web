pipeline {
agent { label 'MASTER' }
parameters {
choice(choices: ['inventory', 'inventorypm'], description: '', name: 'INV_FILE')
choice(choices: ['all', 'DEV', 'SIT', 'UATSEC', 'PERF', 'PREPROD', 'PROD', 'PRODA', 'PRODB'], description: '', name: 'INV_GRP')
}
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

        stage ('Build') {
            steps {
                sh '/usr/local/bin/mvn install' 
            }
        }
    }
}
