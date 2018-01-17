# Ansible Role: libvirtd

Install libvirtd, configure bridge, create guest VM.

## Example playbook

```
- hosts: all
  roles:
    - jblunck.libvirtd
```

Inside `vars/main.yml`:
```
libvirtd_guests:
    - name: centos7
      url: http://mirror.centos.org/centos/7/os/x86_64/
      cpu: 1
      mem: 2048
      virt_type: kvm
      virt_hypervisor: hvm
      os:
          type: linux
          variant: rhel7
      disk:
          size: 5
          path: /var/lib/libvirt/images
      ks: ks.cfg.j2

```
