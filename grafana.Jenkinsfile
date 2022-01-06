def git_url = 'https://github.com/newbielinux1/K8-deployement.git'
def git_branch = 'main'

pipeline
{
    agent
    {
        label 'worker1'
    }

    stages
    {
        stage('deploy')
        {
            
            steps{
                   sh '''
                   pwd
                   ls -ltr
                   mkdir -p /opt/grafana
                   chmod 777 /opt/grafana
                   kubectl delete -f grafana-deploy.yml | exit 0
                   kubectl apply -f grafana-deploy.yml
                   '''
               }
        
        }
    }
}
