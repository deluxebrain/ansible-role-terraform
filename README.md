# Role Name: TERRAFORM

[![Build Status](https://travis-ci.org/deluxebrain/ansible-role-terraform.svg?branch=master)](https://travis-ci.org/deluxebrain/ansible-role-terraform)

Terraform and TFLint installer for Linux.

## Requirements

None.

## Role Variables

All of the listed variables are defined in `defaults/main.yml`.
Individual variables can be set or overridden by setting them in a playbook for this role.

- `terraform_version`: ( default: latest )
  - Terraform version to install
- `terraform_install_dir`: ( default: /usr/local/bin )
  - Terraform installation directory
- `install_tflint`: ( default: yes )
  - Whether to install TFLint
- `tflint_version`: ( default: latest )
  - TFLint version to install
- `tflint_install_dir`: ( default: /usr/local/bin )
  - TFLint installation directory

## Dependencies

None.

## Example Playbook

```yaml
- hosts: servers
  roles:
      - deluxebrain.terraform
        terraform_version: 0.12.18
        tflint_version: 0.13.4
```

## Development Installation

Packages are split into development and production dependencies, which are managed through the included files `requirements-dev.txt` and `requirements.txt` respectively.

Production packages are managed through the `pip-tools` suite, which installs and synchronizes the project dependencies through the included `requirements.in` file.

```sh
# Create project virtual environment
# Install development dependencies into virtual environment
make install
```

`pip-tools` is responsible for the generation of the `requirements.txt` which is a fully pinned requirements file used for both synchronizing the Python virtual environment and for the installation of packages within a production environment.

Note that this means that the `requirements.txt` file *should not be manually edited* and must be regenerated every time the `requirements.in` file is changed. This is done as follows, which also synchronizes any package changes into the virtual environment:

```sh
# Compile the requirements.in file to requirements.txt
# Install the requirements.txt pacakges into the virtual environment
make sync
```

`pip-tools` and other development requirements are installed through the `requirements-dev.txt` file, as follows:

## License

MIT / BSD

## Author Information

This role was created in 2020 by [deluxebrain](https://www.deluxebrain.com/).
