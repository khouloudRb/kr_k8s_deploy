node {
    stage('clone'){
        checkout([$class: 'GitSCM',
         branches: [[name: '*/main']],
         userRemoteConfigs: [[url: 'https://github.com/khouloudRb/kr_k8s.git']]])
    }
    stage('Apply Kubernetes files') {
        withKubeConfig([credentialsId: '31cd8975-75f2-4c55-bb79-c1e0af38a721']) {
            sh 'kubectl get -- all'
            sh 'kubectl apply -f database.yaml'
            sh 'kubectl apply -f server.yaml'
            sh 'kubectl apply -f client.yaml'
            sh 'kubectl apply -f ingress.yaml'
            sh 'kubectl get -- all'
            
        }
        
    }
}
