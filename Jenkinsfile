pipeline{
    agent any
    stages{
        stage("1"){
            environment { 
                w1 = 1
                w2 = 1
            }
            steps{ 
            
            sh "echo $w1"
            sh "echo ${w1}"
            kubernetesDeploy(
                    kubeconfigId: 'kubeconfig',
                    configs: 'env.yaml',
                    enableConfigSubstitution: true
                )
              sh "cat env.yaml"
            
            }
        }
    }
}
