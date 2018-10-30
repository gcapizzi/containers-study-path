# Introduction

Hello, and welcome to this tutorial!

During this journey you will, hopefully, get a better understanding of what Linux containers are and how they work.

We will achieve this by building a simple container engine together, incrementally, implementing new features as we introduce the necessary kernel primitives.

# Containers: why?

* how we used to ship software:
  - copy-and-paste deployments
  - JARs
  - VMs?
  - ...
* the problems we had:
  - "runs on my machine"
  - lack of isolation
* containers as the solution

# Containers do not exist

* containers are just an abstraction over some kernel primitives
  - this is not necessarily a bad thing!
* the building blocks of a Linux container
  - namespaces
  - cgroups
  - filesystems?

# Running a process

* running a process
* returning the process exit code
* the UTS namespace

# Getting our own root

* mount namespaces
* `chroot` vs `pivot_root`

# Limiting our CPU usage

* the `cpuset` cgroup

# Limiting our memory usage

* the `memory` cgroup

# Making our filesystem changes ephemeral

* `overlay` filesystems
* using a loopback device?

# What happens in Vegas stays in Vegas

* the PID namespace
* mounting the `proc` virtual filesystem to fix `ps`

# Sharing folders with the host

* bind-mounts

# Signaling containerised processes?

* `pdeathsig`?
* signal handling in Go?
* subreaper?

# Devices

* mounting the `dev` virtual filesystem
