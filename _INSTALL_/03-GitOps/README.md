Pro spravnou funkci ArgoCD je potreba vytvorit clusterrolebinding na ACM objekty


$ oc adm policy add-cluster-role-to-user open-cluster-management:subscription-admin system:serviceaccount:openshift-gitops:openshift-gitops-argocd-application-controller
