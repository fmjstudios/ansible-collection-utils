# Ansible Role: Upgrades

This role updates all packages, autoclean's unneeded ones and configures automatic unattended upgrades with the default values specified.

## Requirements

N/A

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

``` yaml
# Debian
apt_upgrade_package_lists_days: 1
apt_unattended_upgrade_days: 1
apt_download_upgradeable_days: 3
apt_autoclean_days: 7

# RedHat
conf_download_update: yes
conf_apply_update: yes
```

## Dependencies

None.

## Example Playbook

```yaml
    - hosts: all
      roles:
        - role: upgrades
```

## License

Proprietary

## Author Information

This role was created in 2023 by [Maximilian Gindorfer](https://fmj.dev).
