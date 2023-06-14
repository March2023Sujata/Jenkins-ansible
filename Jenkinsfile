pipeline{
    agent { label 'Node'}
    stages{
        stage('VCS'){
            steps{
                git url: 'https://github.com/March2023Sujata/Jenkins-ansible.git',
                    branch: 'main'
            }
        }
        stage('ansible-playbook'){
            steps{
                dir('ansible'){
                    sh 'ansible-playbook -i hosts nop.yml'
                }
            }
        }
    }
}