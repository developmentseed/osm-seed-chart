# osm-seed Helm chart repository

Helm repository for the [osm-seed](https://github.com/osm-seed/osm-seed) chart, published
at https://osm-seed.github.io/osm-seed-chart.

```sh
helm repo add osm-seed https://osm-seed.github.io/osm-seed-chart
helm repo update
helm install osm osm-seed/osm-seed -f myvalues.yaml
```

Do not edit this repository by hand. Every push to `develop` in
[osm-seed/osm-seed](https://github.com/osm-seed/osm-seed) runs
[chartpress](https://github.com/jupyterhub/chartpress), which packages the chart, adds it
to `index.yaml` and commits here. The `gh-pages` branch is served by GitHub Pages with a
Jekyll page that lists the published versions.

Chart documentation and values: [osm-seed/osm-seed/README.md](https://github.com/osm-seed/osm-seed/blob/develop/osm-seed/README.md).
