node('kube-agent') {
        stage("CD:"){
            
         container('deployer'){
             
            stage("Clone Git Repository") {
          
                git(
                    url: "https://github.com/moh-amer/graduation_config",
                    branch: "main",
                    changelog: true,
                    poll: true
                )
             }
        
                  stage("Deploy the app") {
                      
                     sh "kubectl apply -f ."
             }
        }
    }
}
