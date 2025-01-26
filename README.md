Create a jenkins namespace before running the below command
kubect create namespace jenkins

  argocd app create jenkins `
  --repo https://github.com/judexman01/myjenkins.git `
  --path . `
  --dest-server https://kubernetes.default.svc `
  --dest-namespace jenkins `
  --sync-policy automated
