# Changes

This document main purpose is to list changes which might affect backwards compatibility. It will not list all releases as Eclipse JKube is build in a continous delivery fashion.

We use semantic versioning in some slight variation until our feature set has stabilized and the missing pieces has been filled in:

* The `MAJOR_VERSION` is kept to `0`
* The `MINOR_VERSION` changes when there is an API or configuration change which is not fully backward compatible.
* The `PATCH_LEVEL` is used for regular CD releases which add new features and bug fixes.

After this we will switch probably to real [Semantic Versioning 2.0.0](http://semver.org/)

## Extracting changelog portions
We provide a script to extract changelog portions and automatic link building to send notifications
(i.e. e-mail) about new releases
([scripts/extract-changelog-for-version.sh](https://github.com/eclipse/jkube/blob/master/scripts/extract-changelog-for-version.sh))

Usage:
```
# ./scripts/changelog.sh semanticVersionNumber [linkLabelStartNumber]
./scripts/extract-changelog-for-version.sh 1.3.37 5
```
### 1.0.0-alpha-SNAPSHOT
* Fix #182: Assembly is never null
* Fix #198: Wildfly works in OpenShift with S2I binary build (Docker)

### 1.0.0-alpha-3 (2020-05-06)
* Fix #167: Add CMD for wildfly based applications
* Added Webapp Wildfly maven quickstart
* Fix #171: OpenShift pull secret not picked up without registry auth configuration
* Fix #171: Customized Quarkus application quick start
* Fix #101: Removed OpenShift specific functionality from Kubernetes Maven Plugin
* Fix #178: Bump kubernetes-client from 4.9.1 to 4.10.1

### 1.0.0-alpha-2 (2020-04-24)
* Fix #130: Updated HelmMojo documentation
* Fix #138: dockerAccessRequired should be false in case of docker build strategy
* Fix #131: Extra-artifact wrongly generated
* Fix #152: kubernetes namespace is ignored in debug goal
* Ported PR fabric8io/fabric8-maven-plugin#1810, Update Fabric8 Images to latest version
* Fix #136: Refactored configuration model to provide fluent builders and defaults
* Fix #163: Added Quickstart for external Dockerfile

### 1.0.0-alpha-1 (2020-03-27)
* Ported PR fabric8io/fabric8-maven-plugin#1792, NullCheck in FileDataSecretEnricher
* Fix #53: Renamed plugins to openshift/kubernetes-maven-plugin keeping acronym (oc/k8s) for goal
* Fix #97: Port of fabric8io/fabric8-maven-plugin#1794 to fix ImageChange triggers not being set in DeploymentConfig when resource fragments are used
* Ported PR fabric8io/fabric8-maven-plugin#1802, Labels are missing for some objects
* Ported PR fabric8io/fabric8-maven-plugin#1805, NullPointerException in ConfigMapEnricher
* Ported PR fabric8io/fabric8-maven-plugin#1772, Support for setting BuildConfig memory/cpu request and limits 
* Fix #112: Fix windows specific path error while splitting file path
* Fix #102: HelmMojo works again
* Fix #120: Critical bugs reported by Sonar
* Fix #88: Unreachable statement in DockerAssemblyManager
* Fix #122: Bug 561261 - jkube-kit - insecure yaml load leading to RCE (CWE-502)

### 0.2.0 (2020-03-05)
* Fix #71: script to extract changelog information for notifications
* Fix #34: Ported OpenLiberty support: https://github.com/fabric8io/fabric8-maven-plugin/pull/1711
* Fix #76: Github actions checkout v2
* Updated Kubernetes-Client Version to 4.7.1 #70
* Fix #30: Decouple JKube-kit from maven
* Fix #87: JKubeAssemblyFile is processed
* Fix #89: Reorganized Quickstarts + Added PR verifications (versionable and compilable)
* Fix #92: NullPointerException in AuthConfigFactory
* Fix #89: Reorganized examples + fixed assembly bug
* Fix #52: Use proper case in JKube brand name
* Doc #43: added default md file and links for CONTRIBUTING guide
* Doc #61: Added a Hello World Quickstart sample
* Fix #95: filtered is for variable interpolation/substitution, not for exclusion
* Doc #91: Quarkus Native Quickstart


### 0.1.1 (2020-02-14)
* Refactor: Add Maven Enforcer Plugin #29
* Fixed broken Quarkus Sample #65
* Doc: Added Migration guide for Fabric8 Maven Plugin users #64
* Fix: Problem with plexus detecting target value type for bean injection #62
* Fix: Disable Jolokia, missing PR port from FMP for ThorntailGenerator #60
* Fix: Report consolidation/artifact generation in GitHub Actions #59
* Fix: Docker builds are supported in oc-maven-plugin #56
* Fix: Generated webapp war has wrong name #54
* Feat: Configurable Dekorate integration #36
* Fix: Missing component declaration in Plexus container #41
* Fix: Close input streams + other fixes #41
* Refactor: removed implementations from config/resource -> resource/service #46
* Refactor: jkube-kit-config-image decoupled from Maven #45
* Refactor: Clean up dependencies + enforce version convergence #39
* Doc: Add documentation #38
* Add Sample Quickstarts to project #33
* Fix: Run tests for current version #35

### 0.1.0 (2019-12-19)
* Initial release
