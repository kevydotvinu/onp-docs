# Debug Tools

The debug tools which are available in the OpenShift Network Playground are listed below.

* network-tools
* Kind cluster
* Kind cluster with OVN
* RHCOS Live CD

## Network-tools

> `network-tools` is a collection of tools for debugging OpenShift cluster network issues. It contains both debugging scripts (described in the next section) and useful tools to get information from the cluster. This repo is supposed to be used by network engineers and support to debug and diagnose issues. Customers can also be advised to use commands from this image to help get required information. - [GitHub](https://github.com/openshift/network-tools)

## Kind cluster

> [kind](https://sigs.k8s.io/kind) is a tool for running local Kubernetes clusters using Docker container “nodes”.\
> kind was primarily designed for testing Kubernetes itself, but may be used for local development or CI. - [https://kind.sigs.k8s.io/](https://kind.sigs.k8s.io/)

In OpenShift Network Playground Kind uses `podman` rather than `docker`.

## Kind cluster with OVN

> KIND (Kubernetes in Docker) deployment of OVN kubernetes is a fast and easy means to quickly install and test kubernetes with OVN kubernetes CNI. The value proposition is really for developers who want to reproduce an issue or test a fix in an environment that can be brought up locally and within a few minutes. - [https://github.com/openshift/ovn-kubernetes](https://github.com/openshift/ovn-kubernetes)

## RHCOS Live CD

It enables the user to create a VM with a separate network and interact with the cluster for some issue reproducers.
