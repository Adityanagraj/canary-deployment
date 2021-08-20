
node{
        env.w1 = 10
        env.w2 = 20
        stage("1"){
            
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

