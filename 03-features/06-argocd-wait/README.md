# argocd-wait (v1.10)

Demonstrates the new `argocd-wait` step that blocks a promotion until an
Argo CD Application reaches desired health status, without triggering a sync.

This is useful when gating on application health driven by ArgoCD's own
auto-sync, rather than explicitly triggering a sync via `argocd-update`.
The pattern: update the target revision, then wait for ArgoCD to sync and
become healthy on its own.
