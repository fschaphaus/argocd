apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: <name>>
  namespace: argocd
spec:
  destination:
    namespace: default
    server: https://kubernetes.default.svc
  project: system-components
  source:
    path: helm-guestbook
    repoURL: https://github.com/argoproj/argocd-example-apps.git
    targetRevision: HEAD
