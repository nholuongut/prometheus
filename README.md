# Prometheus

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

<!-- INDEX_START -->

- [Quick Prometheus Doc](#quick-prometheus-doc)
- [Prometheus Management Code](#prometheus-management-code)
  - [Initialize DevOps-Bash-tools and Template git submodules](#initialize-devops-bash-tools-and-template-git-submodules)
  - [Prometheus](#prometheus)
    - [Download and install Prometheus locally quickly](#download-and-install-prometheus-locally-quickly)
    - [Download Quick Sample Config from nholuongut/templates](#download-quick-sample-config-from-nholuonguttemplates)
    - [Run Prometheus](#run-prometheus)
  - [Prometheus Exporters](#prometheus-exporters)
    - [Install Node Exporter](#install-node-exporter)
    - [Run Node Exporter](#run-node-exporter)
  - [Systemd Unit Files](#systemd-unit-files)
- [More Core Repos](#more-core-repos)
  - [Knowledge](#knowledge)
  - [DevOps Code](#devops-code)
  - [Containerization](#containerization)
  - [CI/CD](#cicd)
  - [DBA - SQL](#dba---sql)
  - [DevOps Reloaded](#devops-reloaded)
  - [Templates](#templates)
  - [Misc](#misc)

<!-- INDEX_ENDF -->

## Quick Prometheus Doc

See the [Prometheus](https://github.com/nholuongut/knowledge-base/blob/main/prometheus.md) page
in the [nholuongut/knowledge-base](https://github.com/nholuongut/knowledge-base) repo.

## Prometheus Management Code

### Initialize DevOps-Bash-tools and Template git submodules

```shell
make init
```

or

```shell
git submodule update --init --recursive
```

### Prometheus

#### Download and install Prometheus locally quickly

```shell
bash-tools/install/install_prometheus.sh
```

#### Download Quick Sample Config from nholuongut/templates

[nholuongut/templates - prometheus.yml](https://github.com/nholuongut/templates/blob/master/prometheus.yml)

```shell
wget https://raw.githubusercontent.com/nholuongut/templates/refs/heads/master/prometheus.yml
```

#### Run Prometheus

Run Prometheus locally, installing it if not already installed:

```shell
bash-tools/monitoring/prometheus.sh
```

Or using [Ansible](https://github.com/nholuongut/Ansible) (Linux only):

```shell
ansible-playbook -i localhost, ansible/prometheus/playbook.yml
```

Or to run it in Docker using docker-compose:

```shell
bash-tools/monitoring/prometheus_docker.sh
```

Open <http://localhost:9090> URL to see Prometheus UI.

This script opens it using whatever the default browser on your Mac or Linux system is:

```shell
bash-tools/bin/urlopen.sh http://localhost:9090
```

Add exporters like the local Node Exporter the sample config is expecting using the next section.

### Prometheus Exporters

To install an exporter, run the relevant install script from here:

#### Install Node Exporter

```shell
bash-tools/install/install_prometheus_node_exporter.sh
```

Or using [Ansible](https://github.com/nholuongut/Ansible) (Linux only):

```shell
ansible-playbook -i localhost, ansible/prometheus_node_exporter/playbook.yml
```

#### Run Node Exporter

Run Prometheus Node Exporter locally, installing it if not already installed:

```shell
bash-tools/monitoring/prometheus_node_exporter.sh
```

### Systemd Unit Files

Systemd unit files for running Prometheus and Node Exporter are available under [systemd](https://github.com/nholuongut/prometheus/blob/main/systemd/).

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)
* [PayPal.me](https://www.paypal.com/paypalme/nholuongut)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟