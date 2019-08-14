# grub2

This role configures grub 2 and rebuilds the config in /boot.

## Requirements

Debian

## Role Variables

| Name                 | Default / Mandatory | Description                                    |
|:---------------------|:-------------------:|:-----------------------------------------------|
| `grub2_default_conf` | `{}`                | Configuration to write to `/etc/default/grub2` |
| `grub2_os_prober`    | `true`              | Whether to enable the os-prober                |

## Example Playbook

```yml
- hosts: physical
  roles:
    - role: grub2
      grub2_os_prober: false
      grub2_default_conf:
        GRUB_CMDLINE_LINUX: console=tty0 console=ttyS0,115200
```

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

## Author Information

- [Janne Heß](https://github.com/dasJ)
