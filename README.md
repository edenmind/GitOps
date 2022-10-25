# Flux

## Installation

Flux has been installed using: <https://fluxcd.io/docs/get-started/>

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
