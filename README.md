# helm-chart for osm-seed

This repository stores in its gh-pages branch packaged Helm charts for osm-seed K8s. These packaged Helm charts are made available from https://github.com/developmentseed/osm-seed thanks to Github Actions and this Helm chart repository has automatically updated with the latest versions of the charts: https://devseed.com/osm-seed-chart/.

## Local development of GitHub page


```sh
    git clone git@github.com:developmentseed/osm-seed-chart.git
    git checkout gh-pages

    # Make sure that index.yaml is link to _data/
    mkdir _data
    cd _data
    ln -s ../index.yaml index.yaml
    cd ..

    # Install Jekyll
    bundle install
    
    # Start a local webserver
    bundle exec jekyll serve --livereload
```

Visit http://localhost:4000.