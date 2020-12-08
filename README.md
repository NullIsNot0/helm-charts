# Making a release
Create a separate directory for each release code.

## Lint
```bash
helm lint source/local-path-provisioner/0.0.19
helm lint source/nfs-client-provisioner/1.2.11
```

## Package
```bash
helm package source/local-path-provisioner/0.0.19 -d release/local-path-provisioner
helm package source/nfs-client-provisioner/1.2.11 -d release/nfs-client-provisioner
```

## Generate Index
```bash
helm repo index release --url https://nullisnot0.github.io/helm-charts/release
```

## Publish
Add, Commit and Push to GitLab.
