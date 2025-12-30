learning gitops tools ArgoCD from scratch, using minikube for this tutorial
1) Install ArgoCD
  kubectl create namespace argocd
  kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

2) Steps to access argocd UI from browser
  i) Edited argocd-server service from clusterIP type to NodePort so that i can access argocd UI through my browser
  ii) minikube service argocd-server -n argocd         it will create a tunnel & start argocd server so that we can connect it through browser
  iii) Now getting the password for argocd ui
       kubectl get secret -n argocd
       kubectl edit secret argocd-initial-admin-secret -n argocd       now in this secret there is a password copy that one & decode it & then you can use that pass to login into argocd ui
       joh mera minikube uska pass - 7RykTmJFjhb55-0G

3) we can access argocd with CLI too, tutorial is available anywhere
   
