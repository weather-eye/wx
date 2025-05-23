# wx

[![forthebadge](https://forthebadge.com/images/badges/built-by-developers.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com)

[![python3](https://img.shields.io/badge/python-3.6%20%7C%203.7%20%7C%203.8-brightgreen.svg)](https://python3statement.org/#sections50-why)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)
[![security: bandit](https://img.shields.io/badge/security-bandit-yellow.svg)](https://github.com/PyCQA/bandit)

## About

WeatherEye Controller (wx) is a single codebase, implemented using the Python Textualize package, that provides a Command Line Interface (CLI), Text User Interface (TUI) and Web UI for [provisioning](https://www.redhat.com/en/topics/automation/what-is-provisioning) (Terraform), [orchestrating](https://www.redhat.com/en/topics/automation/what-is-orchestration) (Ansible) and configuring WeatherEye software on Linux servers.

`wx` is aware of environments that it can install to including:
1. Provisioning
    - Infrastructure Providers (e.g. Locally [Proxmox](https://github.com/Telmate/terraform-provider-proxmox) or [VMWare](https://registry.terraform.io/providers/hashicorp/vsphere/latest). Remote: Amazon Web Services, Google Cloud Platform etc. see [supported providers](https://registry.terraform.io/search/providers)
2. Orchestrating
    - Linux servers (VMs, cloud instances) 
3. Configuration Management
    - WeatherEye Admin Django project (configuring which Django apps are running in a single Django instance)
    - Other WeatherEye application configurations

The `wx` command line tool includes the following modules which can also be accessed through WeatherEye Admin:
- WeatherEye Upgrade
- WeatherEye Rollback
- WeatherEye Backup

---
*Powered by:*
- [Terraform](https://developer.hashicorp.com/terraform) for [server provisioning](https://www.redhat.com/en/topics/automation/what-is-provisioning)
- [Ansible](https://docs.ansible.com/) for [server orchestration](https://www.redhat.com/en/topics/automation/what-is-orchestration)
- [Textualize](https://www.textualize.io/) (MIT) - An application framework for CLI, TUI and WebUI in a single codebase
- [pipx](https://pipx.pypa.io/stable/) - A way to install Python CLI's as a tool in a contained environment

### Tests

Run `pytest`. For more detailed output, including test coverage:

```sh
pytest -vv --cov=. --cov-report term-missing
```

### Contributing

If you would like to contribute to the project:

- if you're making code contributions, please try and write some tests to accompany your code, and ensure that the tests pass.
- commit your changes via `cz commit`. Follow the prompts. When you're done, `pre-commit` will be invoked to ensure that your contributions and commits follow defined conventions. See `pre-commit-config.yaml` for more details.
- your commit messages should follow the conventions described [here](https://www.conventionalcommits.org/en/v1.0.0/). Write your commit message in the imperative: "Fix bug" and not "Fixed bug" or "Fixes bug." This convention matches up with commit messages generated by commands like `git merge` and `git revert`.
Once you are done, please send a [merge request](https://docs.gitlab.com/ee/user/project/merge_requests/).

