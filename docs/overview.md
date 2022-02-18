# Istio Operator

## Overview

This package contains a configurable installation of the Istio Operator based on the upstream chart provided by Istio.

## Istio Operator

[Istio Operator](https://github.com/istio/istio/tree/master/operator) is an open source operator that manages Istio service mesh installations, updates, and deletes in a deployed environment. Updates to the operator custom resource will apply the corresponding configuration changes.

## How it works

`IstioOperator` is a custom resource that describes the desired stated of an Istio installation. The Istio Operator package/deployment manages and maintains the Istio service mesh installation based on the creation, deletion, and modification of any `IstioOperator` custom resources in the cluster. 

Please review the BigBang [Architecture Document](https://repo1.dso.mil/platform-one/big-bang/bigbang/-/blob/master/charter/packages/istio/Architecture.md) for more information about Istio's role within BigBang.

