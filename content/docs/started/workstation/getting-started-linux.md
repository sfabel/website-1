+++
title = "Kubeflow on Linux"
description = "Install Kubeflow on Linux"
weight = 10
+++

### MicroK8s

[MicroK8s](https://microk8s.io) runs natively on most Linux distributions. You can enable Kubeflow with a single command once Microk8s has been installed. MicroK8s supports GPU acceleration as an option. You can select a specific Kubernetes version with the ``--channel`` option (see ``snap info microk8s`` to view all available channels).

```
sudo snap install microk8s --classic --channel=1.15/stable
microk8s.enable gpu
microk8s.enable kubeflow
```

MicroK8s will resolve all dependencies automatically and start Kubeflow on the local machine.

Follow the installation guide for [Kubeflow with MicroK8s](/docs/other-guides/virtual-dev/getting-started-multipass/) to set up MicroK8s and enable Kubeflow in Ubuntu virtual machines.

### MiniKF

MiniKF is a predefined virtual machine that installs onto VirtualBox through Vagrant.
The only following applications are required to use MiniKF:

- Install [Vagrant](https://www.vagrantup.com/downloads.html)
- Install [Virtual Box](https://www.virtualbox.org/wiki/Downloads)

The full set of instructions are available on the
[MiniKF getting started](/docs/other-guides/virtual-dev/getting-started-minikf/) page.
