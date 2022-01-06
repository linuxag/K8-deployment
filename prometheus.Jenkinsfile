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
        stage('k8-deploy')
        {
            
            steps{
                   sh '''
                   mkdir -p /opt/prometheus
                   chmod 777 /opt/prometheus
                  kubectl apply -f prometheus-configmap.yml
                  kubectl apply -f prometheus-deploy.yml
                  
                   '''
               }
        
        }
    }
}