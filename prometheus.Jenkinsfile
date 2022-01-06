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
                  kubectl delete -f prometheus-configmap.yml | exit 0
                  kubectl apply -f prometheus-configmap.yml
                  kubectl delete -f prometheus-deploy | exit 0
                  kubectl apply -f prometheus-deploy.yml
                  
                   '''
               }
        
        }
    }
}