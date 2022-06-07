# Metricbeat Ansible role
![Logo](logo.gif)

[![Build Status](https://app.travis-ci.com/idealista/metricbeat_role.svg)](https://app.travis-ci.com/github/idealista/metricbeat_role)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-idealista.metricbeat_role-B62682.svg)](https://galaxy.ansible.com/idealista/metricbeat_role)



This ansible role installs [Metricbeat](https://www.elastic.co/guide/en/beats/metricbeat/current/index.html) in a Debian environment. It has been tested for the following Debian versions:
* Bullseye
* Buster

This role has been generated using the [cookiecutter](https://github.com/cookiecutter/cookiecutter) tool, you can generate a similar role that fits your needs using this [cookiecutter template](https://github.com/idealista/cookiecutter-ansible-role).

- [Getting Started](#getting-started)
	- [Prerequisites](#prerequisites)
	- [Installing](#installing)
- [Usage](#usage)
- [Testing](#testing)
- [Built With](#built-with)
- [Versioning](#versioning)
- [Authors](#authors)
- [License](#license)

## Getting Started
These instructions will get you a copy of the role for your Ansible playbook. Once launched, it will install Metricbeat in a Debian system.

### Prerequisites

Minimum Ansible version of 2.10.0 and recommended Ansible 5.8.0 version installed. 

For testing purposes, [Molecule](https://molecule.readthedocs.io/) with [Docker](https://www.docker.com/) as driver and [Goss](https://github.com/aelsabbahy/goss) as verifier.

### Installing

Create or add to your roles dependency file (e.g requirements.yml):

```
- src: idealista.metricbeat_role
  version: 1.0.0
  name: metricbeat_role
```

Install the role with ansible-galaxy command:

```
ansible-galaxy install -p roles -r requirements.yml -f
```

Use in a playbook:

```
---
- hosts: someserver
  roles:
    - role: metricbeat_role
```

## Usage

Look to the [defaults](defaults/main.yml) properties file to see the possible configuration properties, it is very likely that you will not need to override any variables.


## Testing

### Install dependencies

```sh
$ pipenv sync
```

For more information read the [pipenv docs](https://pipenv-fork.readthedocs.io/en/latest/).

### Test

```sh
$ pipenv run molecule test 
```

## Built With

![Ansible](https://img.shields.io/badge/ansible-5.8.0-green.svg)
![Molecule](https://img.shields.io/badge/molecule-3.6.1-green.svg)
![Goss](https://img.shields.io/badge/goss-0.3.18-green.svg)

## Versioning

For the versions available, see the [tags on this repository](https://github.com/idealista/metricbeat_role/tags).

Additionally, you can see what change in each version in the [CHANGELOG.md](CHANGELOG.md) file.

## Authors

* **Idealista** - *Work with* - [idealista](https://github.com/idealista)

See also the list of [contributors](https://github.com/idealista/metricbeat_role/contributors) who participated in this project.

## License

![Apache 2.0 License](https://img.shields.io/hexpm/l/plug.svg)

This project is licensed under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) license - see the [LICENSE](LICENSE) file for details.
