# RedHat Advance Cluster Management

### Funkcionalita
Advance Cluster Management je v tomto pripade zamyslen jako management nasazovani aplikaci napric ruznymi clustery. V celem flow je co nejvice vyuzivano GitOps pristupu pro nasazovani jednotlivych aplikaci. Centralni HUB cluster jako ridici rovina ma deployovane nasledujici komponenty
- Advance Cluster Management
  - Multicluster
  - Observability
- GitOps operator (ArgoCD)

### Infrastruktura
- HUB cluster
  - Advance Cluster Management
  - GitOps Operator (ArgoCD)
- Imported Clusters
  - GitOps Operator (ArgoCD)
  - Project Operator

#### Popis FLOW
Pomoci GitOps operatora jsou do HUBu nasazovany jednotlive aplikace (Application.app.k8s.io), ktere jsou dale distribuovany pomoci ACM na spravovane clustery.
Aplikace se sklada z nekolika komponent, nicmene finalne ukazuje na artefakty (Git, Helmchart), kde se nachazi konkretni manifesty pro nasazeni.
