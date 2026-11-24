# Helm Charts

A collection of Helm charts, published as a Helm repository on GitHub Pages.

## Usage

```bash
helm repo add helm-charts https://kheav-kienghok.github.io/helm-charts
helm repo update
helm search repo helm-charts
```

Install a chart:

```bash
helm install <release> helm-charts/<chart> -n <namespace> --create-namespace
```

Show a chart's configurable values:

```bash
helm show values helm-charts/<chart>
```

## Layout

```
helm-charts/
├── <chart>/          # chart source
├── <chart>-x.y.z.tgz # packaged charts
├── index.yaml        # Helm repo index
└── LICENSE
```

## Publishing

```bash
helm package <chart>
helm repo index . --url https://kheav-kienghok.github.io/helm-charts
```

Commit the `.tgz` and `index.yaml`, then push. GitHub Pages serves the repo.

## License

[MIT](LICENSE)
