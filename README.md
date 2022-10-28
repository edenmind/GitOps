# GitOps

This repository contains the GitOps configuration for the [OpenArabic project](https://github.com/edenmind/OpenArabic).

## Flux

Flux has been installed using: <https://fluxcd.io/docs/get-started/>

### Good to know

```bash title="Export the GITHUB_TOKEN"
export GITHUB_TOKEN=token
export GITHUB_USER=user
```

```bash title="Install flux"
flux bootstrap github --owner=edenmind --repository=gitops --branch=main --path=./clusters/openarabic
```

```bash title="Add helm source"
flux create source helm openarabic --url=oci://registry.digitalocean.com/openarabic/open-arabic-helm --interval=30s --export > ./clusters/openarabic/openarabic-source.yaml
```
