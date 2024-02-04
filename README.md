# Basic example

## Setup

Update the settings in the inventory file `provisioning/hosts` to match your machines.

## Examples

All examples assume that they are run inside the `provisioning/` directory.

### Run ad-hoc commands

Check the uptime of a single host `www5.wunderbyte.at`:

```sh
ansible -i hosts www5.wunderbyte.at -m command -a uptime
```

Check the uptime of all hosts in the `dev` group:

```sh
ansible -i hosts dev -m command -a uptime
```

Here, `command` is a module and the `-a` argument provides the thing you want to execute.
List disk usage for all `dev` hosts:


```sh
ansible -i hosts dev -m command -a "df -lh"
```
