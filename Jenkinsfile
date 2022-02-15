pipeline {

  agent any

  environment {
   ANSIBLE_PRIVATE_KEY=credentials('ansible-private-key')
  }

  stages {
    stage('Ansible') {
      steps {
        sh 'ansible-playbook -i ansible/inventory --private-key=$ANSIBLE_PRIVATE_KEY ansible/deploy.yml'
      }
    }
  }
