# Chart: Sysdig

## Change Log

This file documents all notable changes to Sysdig Helm Chart. The release numbering uses [semantic versioning](http://semver.org).

## v1.15.41
### Bugfix
* Don't deploy psp policies on k8s 1.25.x

## v1.15.40
### Minor changes
* RuntimeScanner:
    * bump to 1.2.10 version
    * add image size and storage info to warning log

## v1.15.39
### Minor changes
* RuntimeScanner:
	* bump to 1.2.9 version
  	* configurable thresholds for maxFileSize and maxImageSize. Bigger files/images will be skipped
	* logging about the skipping of a file to be analysed changed from error to warning.

## v1.15.38
### Minor changes
* Added cerftificatesigningrequests resources to clusterrole

## v1.15.37
### Minor changes
* HostAnalyzer: fixed certificates issue introduced in 0.1.10

## v1.15.36
### Minor changes
* RuntimeScanner: bumped to 1.2.8 with a fix regarding the dpkg packages version used to match vulnerabilities.

## v1.15.35
### Minor changes
* Security updates (August 2022) for NodeImageAnalyzer and HostAnalyzer components

## v1.15.34
### Minor changes
* RuntimeScanner: bumped to 1.2.7 which:
  * removed the old golang analyzer based on the go.sum files. Only go packages from binary will be analyzed.
  * fixes several bugs in loading images into openshift clusters.
  * improve memory consumption.

## v1.15.32
 ### Minor changes
 * Moved the clusterrole's Ingresses resource to the networking.k8s.io group

## v1.15.31
### Bugfixes
* Don't mount /etc in GKE Autopilot

## v1.15.30
### Minor changes
* RuntimeScanner: version 1.2.6 ignores the fix solution date of a vuln when no fix version is available

## v1.15.29

### Minor changes
* Added /etc to container and initContainer /host/etc volume bind

## v1.15.28

### Minor changes
* Readme fixes

## v1.15.26

### Minor changes
* Agent: Introduced support to proxy for agent initContainer

## v1.15.25

### Minor changes
* reverted change made in v1.15.21 that added /etc to container /host/etc volume bind

## v1.15.24
### Minor changes
* runtimeScanner: version 1.2.5 with fixes on ruby file analyzer

## v1.15.22
### Minor changes
* runtimeScanner: version 1.2.4 with fixes on tmp dirs to be used during analysis

## v1.15.21
### Minor changes
* Added /etc to container /host/etc volume bind

## v1.15.20
### Bugfixes
* Removed duplicate labels from deployment of `app.kubernetes.io/instance`

## v1.15.19
### Minor changes
* runtimeScanner: version 1.2.3 with fixes on java file analyzer


## v1.15.18
### Minor changes
* runtimeScanner: version 1.2.2 with performance improvement in pkgmeta client

## v1.15.17
### Minor changes
* runtimeScanner: version 1.2.0 with fixes on jar manifest parser

## v1.15.16
### Minor changes
* KSPM: version 1.5.0

## v1.15.14
### Minor changes
* Sysdig README file: merged KSPM collector & KSPM analyzer sections

## v1.15.13
### Minor changes
* HostAnalyzer bumped to version 0.1.9 (go 1.18)

## v1.15.12
### Minor changes
* KSPM Analyzer - fix container missing CPU\Memory limits & requests
* KSPM components - Merge analyzer and collector deploy flags into 1
* KSPM Chart components - fix KSPM serviceAccount that is created when KSPM not installed

## v1.15.11
### Minor change
* Security updates (July 2022) for NodeImageAnalyzer and HostAnalyzer component

## v1.15.10
### Minor changes
* Notes section reflects proper links based on deployment region
## v1.15.7
### Minor changes
* BenchmarkRunner: bump tag to 1.0.17.2

## v1.15.6
### Minor changes
* RuntimeScanner version 1.1.1 with Golang support

## v1.15.5
### Minor changes
* Fix expose node name to the Sysdig Agent container through Downward API
  through K8S_NODE environment variable.

## v1.15.2
### Minor changes
* KSPM: add kspmCollector.deploy parameter to docs
* KSPM: bump tag to 1.4.0

## v1.15.1
### Minor changes
* KSPM: bump tag to 1.3.0

## v1.15.0
### Major change
* KSPMAnalyzer: rename cspm-analyzer to kspm-analyzer
* KSPMCollector: rename cspm-collector to kspm-collector

### Minor changes
* KSPMAnalyzer: add documentation on port configuration

## v1.14.34
### Minor changes

* RuntimeScanner: added nodeAnalyzer.runtimeScanner.extraMounts for handle non-standard socket paths

## v1.14.32
### Bugfixes
* RuntimeScanner: enhanced detection of java packages

### Minor changes
* Release of runtime scanner 1.0.4

## v1.14.31
* Describe CSPM components in README and link to official Sysdig docs

## v1.14.3
### Minor change

* CSPMCollector: Handle failure on apis discovery
* CSPMAnalyzer: Send runtime parameters

## v1.14.1
### Minor change

* CSPM support AKS

## v1.14.0
### Major change

* Add CSPM Analyzer to Daemonset and CSPM Collector Deployment

## 1.13.4
### Bugfixes
* RuntimeScanner: added jitter on startup to distribute requests to the k8s api over 15 minutes
* RuntimeScanner: caching data to reduce the amount of requests to the k8s api

### Minor changes
* Release of runtime scanner 1.0.3

## v1.13.1
### Minor change

* Security updates (April 2022) for NodeImageAnalyzer and HostAnalyzer component

## v1.13.0
### Major change

* The slim agent is enabled by default

## 1.12.73
### Bugfixes
* RuntimeScanner: fixed usage of TLS settings when downloading vulnerabilities database
* RuntimeScanner: minor fixes

### Minor changes
* Release of runtime scanner 1.0.1

## 1.12.72
### Bugfixes
* Bugfixes on the runtime scanner

### Minor changes
* Release of runtime scanner 1.0.0

## v1.12.70
### Bugfixes

* Remove the maxSurge field from the rollingUpdate field because not all envs have the new k8s versions

## v1.12.69
### Minor changes

* RuntimeScanner: reduced and better disk usage for temporary files
* RuntimeScanner: added support for Runtime policies

## v1.12.67
### Minor changes

* Add s390x as one of the default architectures for Sysdig Agent node affinity

## v1.12.66
### Minor changes

* Add arm64 as one of the default architectures for Sysdig Agent node affinity

## v1.12.64
### Bugfixes

* RuntimeScanner provides correct image name in containerd environments
* RuntimeScanner provides correct image digest in dockerd environments

## v1.12.63
### Minor changes

* Added CRI-O support for runtime-scanner
* Improved runtime-scanner memory usage
* Updated runtime-scanner to the latest version

## v1.12.61
### Minor changes

 * Fix runtime-scanner `eve_enabled` check in configmap

## v1.12.59
### Minor changes

 * Fix link in README.md

## v1.12.58
### Minor changes

* Add the flag `gke.autopilot` to support the deployment on GKE Autopilot clusters.

## v1.12.57
### Minor changes

* The values for the default affinity settings now come from `daemonset.os` and `daemonset.arch`

## v1.12.55
### Minor changes

* Add dedicated service account for node analyzer

## v1.12.52
### Minor changes

* Fix errors in README.md

## v1.12.51
### Minor changes

* Tech preview release of Runtime Scanner

## v1.12.50
### Minor changes

* Add Runtime Scanner to Daemonset and Eve Connector Deployment

## v1.12.49
### Minor changes

* Bump agent to 12.3.0

## v1.12.48
### Minor changes

* Bump agent to 12.2.1

## v1.12.47
### Bugfixes

* Trim whitespace around image tag

## v1.12.46
### Minor changes

- Add digest value inputs for image pulls

## v1.12.45
### Minor changes

- Add ability to configure affinity and nodeSelector on imageAnalyzer daemonset

## v1.12.43
### Minor changes

- Add a flag to enable/disable Sysdig agent daemonset

## v1.12.41
### Minor changes

- Add custom labels for Sysdig and NodeAnalyzer daemonsets

## v1.12.40
### Minor changes

- Add priorityClassName for NodeAnalyzer

## v1.12.35
### Minor changes

- Removed invalid imagePullSecrets from initContainers

## v1.12.31

### Minor changes

- Add `slim.image.repository` value to allow full slim agent repo name to be configured

## v1.12.30
### Minor changes

- Add strorageclass resource in clusterrole

## v1.12.27

### Minor changes

- Add affinity to nodeImageAnalyzer DaemonSet

## v1.12.26

### Minor changes

- Fix Openshift SCC to allow downward API volumes

## v1.12.25

### Minor changes

- Add priorityclass option for image-analyzer daemonset

## v1.12.24

### Minor changes

- Update agent to 12.0.2

## v1.12.23

### Breaking change notification

- In chart version 1.12.13, the default agent container resources was set to [small](https://docs.sysdig.com/en/tuning-sysdig-agent.html). This was a breaking change (and not minor as originally stated) because upgrading the agent using this chart from an earlier chart where the default was [medium](https://docs.sysdig.com/en/tuning-sysdig-agent.html) could result in less resources configured for it than required.

## v1.12.20

### Minor changes

- Add downward API volume to autodetect agent namespace

## v1.12.16

### Minor changes

- Introduce resource profiles

## v1.12.15

### Minor changes

- Add new resources to ClusterRole to support collection of Kubelet metrics.

## v1.12.14

### Minor changes

- Bump host-analyzer version to 0.1.3

## v1.12.13

### Minor changes

- Change the default agent container resources to [the ones for small clusters](https://docs.sysdig.com/en/tuning-sysdig-agent.html)

## v1.12.12

### Bugfixes

* Add mountPath /sys/kernel/debug for eBPF

## v1.12.11

### Minor changes

- Change the default agent container resources

## v1.12.10

### Minor changes

- Update agent to 11.4.1

## v1.12.9

### Minor changes

- Introduce `leaderelection.enable` for the agent leader election algorithm

## v1.12.8

### Minor changes

- Update values.yaml and README.md to reflect no default value for `nodeAnalyzer.apiEndpoint`

## v1.12.7

### Minor changes

- Update agent to 11.3.0
- Include get/list/create/update/watch leases in agent clusterrole permissions.

## v.1.12.6

### Cleanup

* Rename `nodeAnalyzer.collectorEndpoint` to `nodeAnalyzer.apiEndpoint` to prevent confusion with the Agent collector.
* Update README to reflect deprecation of Node Image Analyzer

### Bugfixes

* Fix `collector_endpoint` in configmap for image-analyzer
* If `nodeImageAnalyzer.settings.collectorEndpoint` is set, deploy old NIA to prevent onboarding instructions from older Sysdig Secure versions from failing.

## v1.12.5

### Bugfixes

* eBPF with Agent slim image did not work on GKE (Google COS)

## v1.12.4

### Bugfixes

* Node analyzer configuration options not being honored due to invalid Configmap name
* Fix `hostBase` for Host Analyzer

## v1.12.3

### Minor changes

* Fix: Respect existingAccessKeySecret in `daemonset-node-analyzer.yaml`
* Update documentation links

## v1.12.2

### Minor changes

* Support eBPF with Agent slim image

## v1.12.1

### Minor changes

* Switch default registry from `docker.io` to `quay.io`
* Update Benchmark Runner to 1.0.6.0
* Correct error in Host Analyzer Configmap

## v1.12.0

### Major changes

* Add Node Analyzer (`nodeAnalyzer.deploy` set to `true` by default)
* Explain all Node Analyzer settings in values.yaml and README, and link to official Sysdig docs
* Disable Node Image Analyzer deployment (`nodeImageAnalyzer.deploy` set to `false` by default)

## v1.11.18

### Minor changes

* Update agent to 11.2.1

## v1.11.17

### Minor changes

* Fix `nodeImageAnalyzer.extraVolumes.volumes` not creating correctly the volumes

## v1.11.16

### Minor changes

* New option `sysdig.existingAccessKeySecret` to use existing or external secrets

## v1.11.15

### Minor changes

* Remove --name installation parameter for `helm install` in README.aws

## v1.11.14

### Minor changes

* Update agent to 11.2.0
* Remove --name installation parameter for `helm install` in README, unsupported in Helm 3.x

## v1.11.13

### Minor changes

* Update agent to 11.1.3

## v1.11.12

### Minor changes

* Fix in probes initialDelay

## v1.11.11

### Minor changes

* Update agent to 11.1.2

## v1.11.10

### Minor changes

* Fix the if in the imageanalyzer extravolumes

## v1.11.9

### Minor changes

* Improvements and fixes in README for installation instructions (use sysdig-agent namespace by default)

## v1.11.8

### Minor changes

* Improvements in CI process and testing

## v1.11.7

### Minor changes

* Update Node Image Analyzer to 0.1.10 by default
* Fix VERIFY_CERTIFICATE setting for Node Image Analyzer

## v1.11.6

### Minor changes

* Add tolerations configuration item to Node Image Analyzer

## v1.11.5

### Minor Changes

* Fix appversion

## v1.11.4

### Minor Changes

* Use the latest image from Agent (11.0.0)

## v1.11.3

### Minor Changes

* Use the latest image from Agent (10.9.0)

## v1.11.2

### Minor changes

* Allow for customization of liveness and readiness probes initial delay

## v1.11.1

### Minor Changes

* Use the latest image from Agent (10.8.0)
* Use the latest image from Node Image Analyzer (0.1.7)

## v1.11.0

### Major changes

* Node Image Analyzer now deployed by default (`nodeImageAnalyzer.deploy` set to `true` by default)
* Explain all Node Image Analyzer settings in values.yaml and README, and link to official Sysdig docs

### Minor changes

* Use the latest image from Agent (10.7.0)
* Change check_certificate to ssl_verify_certificate in NIA settings to sync with NIA configmap

## v1.10.5

* Use the latest image from Node Image Analyzer (0.1.6)

## v1.10.4

* Use the latest image from Agent (10.6.0)

## v1.10.3

### Minor changes

* Add options to add a nodeSelector.

## v1.10.2

### Minor changes

* Use the latest image from Agent (10.5.1)

## v1.10.1

### Minor changes

* Use latest image from Agent (10.5.0)
* Update documentation for agent connection HTTP proxy settings

## v1.10.0

### New features

* Desploy a PSP and the PSP use permission to allow agent running with the required privileges in PSP enabled clusters.

## v1.9.5

### Minor changes

* Use latest image from Agent (10.4.1)

## v1.9.4

### Minor changes

* Use latest image from Agent (10.4.0)

## v1.9.3

### Minor changes

* Redirect to agents dashboard instead of Explore tab.

## v1.9.2

### Minor changes

* Use latest image from Agent (10.3.0)

## v1.9.1

### Minor changes

* Remove explicit *onPrem* option. Use *collectorSettings* section instead.

## v1.9.0

### Major changes

* Option to deploy the [Node Image Analyzer](https://docs.sysdig.com/en/scan-running-images.html).

### Minor changes

* Include get/list/watch endpoints in agent clusterrole permissions.

## v1.8.1

### Minor changes

* Use the latest image from Agent (10.2.0) by default.

### Bug fixes

* Fix logic in template that was disabling captures in the agent settings.

## v1.8.0

### Major changes

* Migrated charts to *sysdiglabs* repository

###  Minor changes

* Add explicit *clusterName* option in values.yaml
* Add beta.kubernetes.io labels for node affinity, to support older versions
* SCC deployed by default in Openshift (check API security.openshift.io/v1)

## v1.7.20

###  Minor changes

* Use the latest image from Agent (10.1.1) by default.

## v1.7.19

###  Minor changes

* Use the latest image from Agent (10.1.0) by default.

## v1.7.18

### Minor changes

* Add explicit *disable captures* option to agent settings.

## v1.7.17

### Minor changes

* Add onPrem as explicit option to set collector host, port and settings
* Fail if no sysdig.accessKey value is provided

## v1.7.16

### Minor changes

* Include support links in README.md

## v1.7.15

### Minor changes

* Use the latest image from Agent (10.0.0) by default.

## v1.7.14

### Minor changes

* Implement a more comprehensive securityContext for running the pod.

## v1.7.13

### Minor changes

* Implement scheduling with affinity and not with nodeSelector on amd64 & linux nodes.
* Add support for custom annotations on daemonSet.

## v1.7.12

### Minor changes

* Use the latest image from Agent (9.9.1) by default.
* Use kubernetes.io/arch label on daemonSet to schedule pods only on amd64 nodes.
* Add a livenessProbe to daemonSet.

## v1.7.11

### Minor changes

* Use app.kubernetes.io labels instead of custom ones

## v1.7.10

### Minor changes

* Use the latest image from Agent (9.9.0) by default.

## v1.7.9

### Minor changes

* Add the SecurityContextConstraints if the security.openshift.io/v1 API is detected.

## v1.7.8

### Minor changes

* Add an image.overrideValue value which is a hack to support
  RELATED_IMAGE_<identifier> feature in Helm based operators.

## v1.7.7

### Minor changes

* Use the latest image from Agent (9.8.0) by default.

## v1.7.6

### Minor changes

* Use rbac.authorization.k8s.io/v1 instead of the beta1 API.
* Fix security key duplication when enabling secure and auditLog.

## v1.7.5

### Minor changes

* Use the latest image from Agent (9.7.0) by default.

## v1.7.4

### Minor changes

* Use the latest image from Agent (9.6.1) by default.

## v1.7.3

### Minor changes

* Removed dependency on ebpf.enabled to set environment variables

## v1.7.2

### Minor changes

* Use the latest image from Agent (9.5.0) by default.

## v1.7.1

### Major changes

* Remove the auditLog.clusterIP dependency. Using dynamic backend allows to
  rely on DNS queries.

## v1.7.0

### Major changes

* Enable Sysdig Secure by default.

## v1.6.0

### Major changes

* Add audit log configuration when deploying the agent.

## v1.5.0

### Major changes

* Add slim configuration for deploying the agent.

### Minor changes

* Mount /etc/modprobe.d from host.
* Drop permissions to read secrets and configmaps.

## v1.4.25

### Minor changes

* Use the latest image from Agent (0.94.0) by default.

## v1.4.24

### Minor changes

* Use the latest image from Agent (0.93.1) by default.

## v1.4.23

### Minor changes

* Update NOTES.txt to use the newest URL for finding the infrastructure.

## v1.4.22

### Minor changes

* Use the latest image from Agent (0.93.0) by default.

## v1.4.21

* Add 'How to upgrade to last version' to the README

## v1.4.20

### Minor changes

* Fixes compatibility errors introduced in v1.4.19.

## v1.4.19

### Minor changes

* Fixes compatibility with kubernetes 1.16.

## v1.4.18

### Minor changes

* Use the latest image from Agent (0.92.3) by default.

## v1.4.17

### Minor changes

* Use the latest image from Agent (0.92.2) by default.

## v1.4.16

### Minor changes

* Allow the DaemonSet to schedule using affinity rules

## v1.4.15

### Minor changes

* Add configmaps and secrets to the resources we can read
* Add support for priorityClassName, httpProxy, timezone and any env variable settings

## v1.4.14

### Minor changes

* Update REAMED.md to fix the example in how to use the `sysdig.settings.tags` in the command line with `--set`

## v1.4.13

### Minor changes

* Use the latest image from Agent (0.92.1) by default.
* Increase `resources.requests` and `resources.limits` to match the [values
  provided by Sysdig's agent team.](https://github.com/draios/sysdig-cloud-scripts/blob/master/agent_deploy/kubernetes/sysdig-agent-daemonset-v2.yaml#L70)

## v1.4.12

### Minor changes

* Use the latest image from Agent (0.92.0) by default.

## v1.4.11

### Minor Changes

* Add nestorsalceda as an approver in the OWNERS file

## v1.4.10

### Minor Changes

* Use the latest image from Agent (0.90.3) by default.

## v1.4.9

### Minor Changes

* Use the latest image from Agent (0.90.2) by default.

## v1.4.8

### Minor Changes

* Add a volume with the os release information.
* Use the latest image from Agent (0.90.1) by default.

## v1.4.7

### Minor Changes

* Add apiVersion to Chart.yaml.

## v1.4.6

### Minor Changes

* Dont allow to change the value of `new_k8s` flag.

## v1.4.5

### Minor Changes

* Enable `new_k8s` flag by default.  This allows kube state metrics to be
  automatically detected, monitored, and displayed in Sysdig Monitor.

## v1.4.4

### Minor Changes

* Use the latest image from Agent (0.89.5) by default.
* Add `persistentvolumes` and `persistentvolumeclaims` to ClusterRole

## v1.4.3

### Minor Changes

* Provide an empty value to `sysdig.accessKey` key.

## v1.4.2

### Minor Changes

* Use the latest image from Agent (0.89.4) by default.
* Use latest shovel logo.

## v1.4.0

### Major Changes

* Use the latest image from Agent (0.89.0) by default.
* eBPF support added.

## v1.3.2

### Minor Changes

* Provide sane defaults resources for the Sysdig Agent.
* Use RollingUpdate strategy by default.

## v1.3.1

### Minor Changes

* Revert v1.2.1 changes. The agent automatically restarts when detects a change in the configuration.

## v1.3.0

### Major Changes

* Use a lower pod termination grace period for avoiding data gaps when pod fails to terminate quickly.
* Check running file on readinessProbe instead of relaying on logs.
* Mount /run and /var/run instead of Docker socket. It allows to access CRI / containerd socket.
* Avoid floating references for the image.

## v1.2.2

### Minor Changes

* Fix value in the agent tags example.

## v1.2.1

### Minor Changes

* Add checksum annotations to DaemonSet so that rolling upgrades works when a ConfigMap changes.

## v1.2.0

### Major Changes

* Allow to use other Docker registries (ECR, Quay ...) to download the Sysdig agent image.

## v1.1.0

### Major Changes

* Add support for uploading custom app checks for Sysdig agent

## v1.0.4

### Minor Changes

* Update README file with instructions for setting up the agent with On-Premise deployments

## v1.0.3

### Minor Changes

* Fixed error in ClusterRoleBinding's roleRef

## v1.0.2

### Minor Changes

* Fix readinessProbe in daemonset's pod spec

## v1.0.1

### Minor Changes

* Add dnsPolicy to daemonset. Its value is ClusterFirstWithHostNet
* Fix link target for retrieving Sysdig Monitor Access Key in README

## v1.0.0

### Major Changes

* Run Sysdig agent as [daemonset v2.0](https://github.com/draios/sysdig-cloud-scripts/blob/master/agent_deploy/kubernetes/sysdig-agent-daemonset-v2.yaml).
* Fix value's naming in order to follow [best practices](https://docs.helm.sh/chart_best_practices/#naming-conventions).
* Use a secure.enabled flag for enabling Sysdig Secure.
* Allow rbac resource creation or use existing serviceAccountName.
* Use required function for retrieving sysdig.accessKey. This ensures that key is present.
