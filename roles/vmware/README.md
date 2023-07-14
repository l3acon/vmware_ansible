# redhatautomation.snow_self_service.vmware

This role builds a virtual machin in a VMWare vCenter environment, exporting data deemed useful for the SNOW Self-Service demonstration.

## Requirements 
The below requirements are needed on the host that executes this role.
* python >= 2.6
* PyVmomi

## Variables
This role expects a variety of variables to be set in order to function. The following is an example with descriptions of each.

```yaml
---
# the domain where the VM will exist
vmware_domain: "some.domain.com"

# the domain where the VM will exist
vmware_esxi_host: "some.domain.com"

# the folder where to put the VM
vmware_folder: "somefolder"

# the virtual environment's DNS servers
vmware_dns_servers: "192.168.0.1"

# the name of the VM to be provisioed
vmware_name: "some_default_name"

# the template to build the VM from
vmware_os_template: "some-os-template"

# a dictionary containing tags for the HW information used to build the VM
vmware_hardware: 
  "lc1.small":
    memory_mb: "2048"
    num_cpus: "2"
  "lc1.medium":
    memory_mb: "4096"
    num_cpus: "4"
  "lc1.large":
    memory_mb: "8192"
    num_cpus: "8"
  "lc1.xlarge":
    memory_mb: "16384"
    num_cpus: "16"
```

## Refernces
* https://github.com/ansible-collections/vmware.vmware_rest
* https://console.redhat.com/ansible/automation-hub/repo/published/vmware/vmware_rest
