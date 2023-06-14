---
description: A lab environment wherein we can test all the OpenShift network scenarios
---

# OpenShift Network Playground Overview

## Overview

The OpenShift Network Playground is both web-based and cli-based interface built for advanced OpenShift users that makes it easy to quickly build and test different OpenShift network scenarios.



OpenShift Network Playground enables you to do the following:

* Zero touch installation
* Deploy an OpenShift Baremetal IPI cluster using an single command.
* Deploy Single-stack or Dual-stack cluster Single Node OpenShift cluster.
* Reproduce all the network related scenarios.
* Store and restore multiple OpenShift releases - Saves deployment time.
* Plug in additional network interface
* Fast reproducer using pre-added manifests
* OpenShift node console access and authentication

## Glossary of common terms for OpenShift Container Platform <a href="#getting-started-openshift-common-terms_openshift-overview" id="getting-started-openshift-common-terms_openshift-overview"></a>

This glossary defines common Kubernetes and OpenShift Container Platform terms.

### Kind

kind is a tool for running local Kubernetes clusters using Docker container "nodes". kind was primarily designed for testing Kubernetes itself, but may be used for local development or CI.

### DNS64

DNS64 is a DNS service that returns AAAA records with these synthetic IPv6 addresses for IPv4-only destinations (with A but not AAAA records in the DNS). This lets IPv6-only clients use NAT64 gateways without any other configuration.

### NAT64

NAT64 is an IPv6 transition mechanism that facilitates communication between IPv6 and IPv4 hosts by using a form of network address translation (NAT).



