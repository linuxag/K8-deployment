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
                  kubectl apply -f proemtheus-configmap.yml
                  kubectl apply -f prometheus-deploy.yml
                  
                   '''
               }
        
        }
    }
}