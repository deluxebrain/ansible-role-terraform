# Role Name: TERRAFORM

[![Build Status](https://travis-ci.org/deluxebrain/ansible-role-terraform.svg?branch=master)](https://travis-ci.org/deluxebrain/ansible-role-terraform)

Terraform installer for Linux.

## Requirements

None.

## Role Variables

All of the listed variables are defined in `defaults/main.yml`.
Individual variables can be set or overridden by setting them in a playbook for this role.

- `terraform_version`: ( default latest ) Terraform version to install
- `terraform_archive_dir`: ( default /usr/local/bin ) Terraform installation directory
- `terraform_archive_path`: ( default /usr/local/bin/terraform ) Terraform installation path
- `tflint_version`: ( default latest ) TFLint version to install
- `tflint_archive_dir`: ( default /usr/local/bin ) TFLint installation directory
- `tflint_archive_path`: ( default /usr/local/bin/terraform ) TFLint installation path

## Dependencies

None.

## Example Playbook

    - hosts: servers
      vars:
        terraform_version: 0.12.18
        tflint_version: 0.13.4    
      roles:
         - deluxebrain.terraform
         

## License

MIT / BSD

## Author Information

This role was created in 2020 by [deluxebrain](https://www.deluxebrain.com/).
