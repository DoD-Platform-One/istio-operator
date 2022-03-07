# Changelog

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
---

## [1.13.1-bb.0]
### Changed
- Updated kptfile
- Accepted reasonable changes made by `kpt pkg update` in Chart.yaml, values.yaml, deployment.yaml and gen-operator.yaml
- Bumped version to `1.13.1-bb.0`

## [1.11.5-bb.1]
### Changed
- Update Chart.yaml to follow new standardization for release automation
- Added renovate check to update new standardization

## [1.11.5-bb.0]
### Changed
- Updated to upstream 1.11.5

## [1.11.3-bb.3]
### Added
- Added OSCAL component for Istio Operator

## [1.11.3-bb.2]
### Changed
-  Remove duplicate image pull policy in the deployment

## [1.11.3-bb.1]
### Changed
-  Added image pull policy for the deployment

## [1.11.3-bb.0]
### Changed
- Updated to 1.11.3 operator version

## [1.11.2-bb.0]
### Changed
- Updated to 1.11.2 operator version

## [1.10.4-bb.1]
### Changed
- Added revision support for canary upgrades

## [1.10.4-bb.0]
### Changed
- Updated Istio to 1.10.4

## [1.10.3-bb.0]
### Changed
- Updated Istio to 1.10.3

## [1.9.7-bb.2]
### Added
- Added template value for istio operator image name

## [1.9.7-bb.1]
### Changed
- Updated resource request and limit to equal values for Guaranteed QOS

## [1.9.7-bb.0]
### Changed
- Updated Istio to 1.9.7

## [1.8.4-bb.2]
### Added
- Added network policies for istio operator
