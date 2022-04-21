# test-argocd  
Microk8sとArgoCDを用いたGitOps 

### インストール
- Microk8s
> https://ubuntu.com/tutorials/install-a-local-kubernetes-with-microk8s?&_ga=2.104564681.850722934.1650062283-880975647.1640664499#1-overview  
- ArgoCD
> https://argo-cd.readthedocs.io/en/stable/getting_started/

### memo
- ArgoCD サーバの初期パスワード取得コマンド  
` sudo microk8s kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d`
- ArgoCD 初期ユーザ名  
`admin`  
- Argocdサーバのアドレス取得  
`sudo microk8s kubectl get all -n argocd`  
- mysql 接続確認  
`sudo microk8s kubectl run -it --rm --image=mysql:5.6 --restart=Never mysql-client -- mysql -h mysql -ppassword`
