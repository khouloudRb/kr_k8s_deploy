# kr_k8s_deploy
Deploy movies App into a minikube cluster. To do so, please follow below steps : 
1. Intsall Kubernetes CLI plugin to jenkins
2. Add k8s credentials to jenkins using the secret file (add config file in .kube)
3. create a new pipeline to deploy the App using the Jenkins files

Note 1 : manifest files are in https://github.com/khouloudRb/kr_k8s_files.git
Note 2 : kubectl get ingress ==> to get the assigned IP address
