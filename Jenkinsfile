pipeline {
    agent any
    parameters {
        choice(name: 'CHOICE', choices: ['TERRAFORM_INIT', 'TERRAFORM_APPLY', 'TERRAFORM_Destroy'], description: 'Pick something')
    stages {
        stage('TERRAFORM_INIT') {
            steps {
                echo 'Running terraform init..'
                sh 'hostname'
                sh 'cd Roboshop_terraform ; terraform init'
            }
        }

    stage('TERRAFORM_APPLY') {
        steps {
               echo 'Running terraform apply..'
               sh 'hostname'
               sh 'terraform apply -auto-approve'
            }
        }

    stage('TERRAFORM_Destroy') {
        steps {
               echo 'Running terraform Destroy..'
               sh 'hostname'
               sh 'terraform destroy -auto-approve'
            }
        }
    }
}