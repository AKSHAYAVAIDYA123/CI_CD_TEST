pipeline{
    agent any
    stages{
        stage('Cleaning Old Code'){
            steps{
                sh 'ssh ec2-user@13.234.113.215 "sudo rm -rf /var/www/html/*"'
            }
        }
        stage('Deploying New Code'){
            steps{
                sh 'scp -r /var/lib/jenkins/workspace/CI_CD_TEST/* ec2-user@13.234.113.215:/var/www/html/'
            }
        }
        stage('Notifying Developers'){
            steps{
                echo 'Email Notification has been sent....'
            }
        }
    }



}