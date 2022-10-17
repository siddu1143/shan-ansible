pipeline{
    agent any
    stages{
        stage ('SCM Checkout'){
            steps {
                git "https://github.com/shanmukhashan022/shan-ansible.git"
            }
        }
        stage('Execute Ansible'){
            steps{
                ansiblePlaybook credentialsId: 'ubuntu11', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'apache.yml'
                }
        }
            
    }    
}
