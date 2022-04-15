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
