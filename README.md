# Istio Operator

Istio operator, chart.

Originaly sourced from [upstream](), and minimally modified.

## Upstream Changes

* optionally remove namespace deployment from chart with `.Values.createNamespace`
* add `imagePullSecrets` with `.Values.imagePullSecrets[]`

## Iron Bank

You can `pull` the registry1 image(s) [here](https://registry1.dsop.io/harbor/projects/3/repositories/opensource%2Fistio-1.7%2Foperator-1.7) and view the container approval [here](https://ironbank.dsop.io/ironbank/repomap/opensource/istio-1.7).