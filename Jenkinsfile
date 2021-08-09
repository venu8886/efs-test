pipeline {
    agent any 
    stages {
        stage('Mount EFS') {
            steps {
                script {
                    sh ''' 
                    cd /tmp/efs-mount-point
                    sudo chown -R jenkins:jenkins ~/efs-mount-point
                    sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport 172.31.12.48:/ .
                    '''
                }
            }
        }
    }
}
