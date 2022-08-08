# How to upgrade the Istio Operator Package chart
1. Checkout the branch that renovate created. This branch will have the image tag updates and typically some other necessary version changes that you will want. You can either work off of this branch or branch off of it. 
1. Run a kpt update to the new version of the Istio Operator chart, typically you can just run `kpt pkg update chart@<version> --strategy alpha-git-patch` (for example `kpt pkg update chart@1.14.3 --strategy alpha-git-patch`)
1. Update the CRD file: `chart/crds/customresourcedefinitions.gen.yaml` is the file to update, there should be a link at the top that takes you to the source file. After navigating there, switch to the correct tag for the new version then copy down the contents + update the link on the first line to the new version.
1. Update version references for the Chart. `version` should be `<version>-bb.0` (ex: `1.14.3-bb.0`) and `appVersion` should be `<version>` (ex: `1.14.3`). Also validate that the BB annotation for the main Istio Operator version is updated (leave the Tetrate version as-is unless you are updating those images).
1. Add a changelog entry for the update. At minimum mention updating the image versions + syncing the upstream chart.
1. Update the readme following the [steps in Gluon](https://repo1.dso.mil/platform-one/big-bang/apps/library-charts/gluon/-/blob/master/docs/bb-package-readme.md).
1. Open MR (or check the one that Renovate created for you) and validate that the pipeline is successful. Also follow the testing steps below for some manual confirmations.

# Testing new Istio Operator version
Generally the operator should be tested alongside the new controlplane version. Follow the steps in the controlplane documentation for testing.

# Modifications made to upstream chart
We do not currently have any modifications documented. A kpt update performed as described above should generally preserve our changes, although we will want to work towards adding this documentation for internal and external developers to reference.
