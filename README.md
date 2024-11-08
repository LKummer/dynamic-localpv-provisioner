# Dynamic Kubernetes Local Persistent Volumes

[![Slack](https://img.shields.io/badge/chat-slack-ff1493.svg?style=flat-square)](https://kubernetes.slack.com/messages/openebs)
[![Community Meetings](https://img.shields.io/badge/Community-Meetings-blue)](https://us05web.zoom.us/j/87535654586?pwd=CigbXigJPn38USc6Vuzt7qSVFoO79X.1)
[![Go Report Card](https://goreportcard.com/badge/github.com/openebs/dynamic-localpv-provisioner)](https://goreportcard.com/report/github.com/openebs/dynamic-localpv-provisioner)
[![FOSSA Status](https://app.fossa.com/api/projects/custom%2B162%2Fgithub.com%2Fopenebs%2Fdynamic-localpv-provisioner.svg?type=shield&issueType=license)](https://app.fossa.com/projects/custom%2B162%2Fgithub.com%2Fopenebs%2Fdynamic-localpv-provisioner?ref=badge_shield&issueType=license)
[![OpenSSF Best Practices](https://www.bestpractices.dev/projects/9666/badge)](https://www.bestpractices.dev/projects/9666)

<img width="300" align="right" alt="OpenEBS Logo" src="https://raw.githubusercontent.com/cncf/artwork/master/projects/openebs/stacked/color/openebs-stacked-color.png" xmlns="http://www.w3.org/1999/html">

<p align="justify">
<strong>OpenEBS Dynamic Local PV provisioner</strong> can be used to dynamically provision 
Kubernetes Local Volumes using different kinds of storage available on the Kubernetes nodes. 
<br>
</p>

## Project Status: GA

Local Persistent Volumes are great for distributed cloud native data services that can handle resiliency and availability and expect low-latency access to the storage. Local Persistent Volumes can be provisioned using the hostpath, NVMe or PCIe based SSDs, Hard Disks or on top of other filesystems like ZFS, LVM. 

Some of the targetted applications are:
- Distributed SQL Databases like PostgreSQL
- Distributed No-SQL Databases like MongoDB, Cassandra
- Distributed Object Storages like MinIO (distributed mode)
- Distributed Streaming services like Apache Kakfa, 
- Distributed Logging and search services like ElasticSearch, Solr
- AI/ML workloads

## Overview 

Kubernetes Local persistent volumes allows users to access local storage through the
standard PVC interface in a simple and portable way. The PV contains node
affinity information that the system uses to schedule pods to the correct
nodes. Features:

- Supports using hostpath as well for provisioning a Local PV. In fact in some
  cases, the Kubernetes nodes may have limited number of storage devices
  attached to the node and hostpath based Local PVs offer efficient management
  of the storage available on the node.

## Kubernetes Compatibility Matrix

|          | Kubernetes <= 1.18 | Kubernetes  1.19 | Kubernetes 1.20 | Kubernetes 1.21 | Kubernetes 1.22 | Kubernetes 1.23 | Kubernetes 1.24 | Kubernetes 1.25 | Kubernetes 1.26 | Kubernetes 1.27 | Kubernetes 1.28 | Kubernetes 1.29 | Kubernetes 1.30 |
|----------|--------------------|------------------|-----------------|-----------------|-----------------|-----------------|-----------------|-----------------|-----------------|-----------------|-----------------|-----------------|-----------------|
| `v4.0.x` | ✕                  | ✓                | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               |
| `v4.1.x` | ✕                  | ✓                | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               |
| `HEAD`   | ✕                  | ✓                | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               | ✓               |

## Install

Please refer to our [Quickstart](https://github.com/openebs/dynamic-localpv-provisioner/blob/develop/docs/quickstart.md) and the [OpenEBS Documentation](http://openebs.io/docs/).

## Contributing

Head over to the [CONTRIBUTING.md](./CONTRIBUTING.md) page.

## Roadmap

Find the Dynamic Local PV roadmap items at the [OpenEBS Roadmap page](https://github.com/openebs/openebs/blob/master/ROADMAP.md#dynamic-local-pvs).

## OpenEBS Adopters

Check out the list of organizations and users who have chosen OpenEBS to run their stateful workloads, over at the [OpenEBS Adopters page](https://github.com/openebs/openebs/blob/master/ADOPTERS.md).

## Community, discussion, and support

Learn how to engage with the OpenEBS community on the [community page](https://github.com/openebs/openebs/tree/master/community).

You can reach the maintainers of this project at:

- [Kubernetes Slack](http://slack.k8s.io/) channels: 
      * [#openebs](https://kubernetes.slack.com/messages/openebs/)
      * [#openebs-dev](https://kubernetes.slack.com/messages/openebs-dev/)
- [Mailing List](https://lists.cncf.io/g/cncf-openebs-users)

### Code of conduct

Participation in the OpenEBS community is governed by the [CNCF Code of Conduct](CODE-OF-CONDUCT.md).

## Inspiration/Credit

OpenEBS Local PV has been inspired by the prior work done by the following the Kubernetes projects:
- https://github.com/kubernetes-sigs/sig-storage-lib-external-provisioner/tree/master/examples/hostpath-provisioner
- https://github.com/kubernetes-sigs/sig-storage-local-static-provisioner
- https://github.com/rancher/local-path-provisioner


## License Compliance
[![FOSSA Status](https://app.fossa.com/api/projects/custom%2B162%2Fgithub.com%2Fopenebs%2Fdynamic-localpv-provisioner.svg?type=large&issueType=license)](https://app.fossa.com/projects/custom%2B162%2Fgithub.com%2Fopenebs%2Fdynamic-localpv-provisioner?ref=badge_large&issueType=license)
