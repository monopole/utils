# Utils

[![Build Status]](https://travis-ci.org/kubernetes/utils)

A set of Go libraries that provide low-level,
kubernetes-independent packages supplementing the [Go
standard libs].

## Purpose

As Kubernetes grows and spins functionality out of its
[core] and into cooperating repositories
like [apiserver], [kubectl], [kubeadm], etc.,
the need arises for leaf repos to house shared code
and avoid cycles in repo relationships.

This repo is intended to hold shared utilities
with no Kubernetes dependence that may be of interest
to any Go project.
  
The [common] repo, on the other hand, holds shared utilities
that may depend on both this repo and other near-leaf
repos like [api].

## Criteria for adding code here

- Used by multiple Kubernetes repos.

- Full unit test coverage.

- Go tools compliant (`go get`, `go test`, etc.).

- Complex enough to be worth vendoring, rather than copying.

- Stable, or backward compatible, API.

- _No dependence on any Kubernetes repo_.

  Code that meets all criteria save this one, e.g.
  functions that depend on Kubernetes [api] types, may
  live in the [common] repo.

[Build Status]: https://travis-ci.org/kubernetes/utils.svg?branch=master
[Go standard libs]: https://golang.org/pkg/#stdlib
[api]: https://github.com/kubernetes/api
[apiserver]: https://github.com/kubernetes/apiserver
[common]: https://github.com/kubernetes/common
[core]: https://github.com/kubernetes/kubernetes
[ingress]: https://github.com/kubernetes/ingress
[kubeadm]: https://github.com/kubernetes/kubeadm
[kubectl]: https://github.com/kubernetes/kubectl

