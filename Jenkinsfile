pipeline {
    agent none

    stages {
        stage('ONE') {
            agent {
                label 'MASTER'
            }
            steps {
                echo 'Testing in master..'
                sh 'hostname'
            }
        }

    stage('TWO') {
        agent {
            label 'workstation'
        }
        steps {
               echo 'Testing in workstation..'
               sh 'hostname'
            }
        }
    }
}