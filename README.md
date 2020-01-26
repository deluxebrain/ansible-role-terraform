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

## License

MIT / BSD

## Author Information

This role was created in 2020 by [deluxebrain](https://www.deluxebrain.com/).
