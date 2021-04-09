# HashiCorp Binaries (hcb)

## Installation

To install, run the following command:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/watsonian/hcb/master/bin/hcb-bootstrap)"
```

This will clone the repository to `$HOME/.hashicorp/hcb` and then run the bootstrap script that will
create all subdirectories that are required. You'll then want to add the following directory to your
PATH:

```
$HOME/.hashicorp/hcb
```

## Usage

After installation, you can install HashiCorp binaries like this:

```
hcb consul 1.9.4
```

If the binary hasn't already been fetched, it will be downloaded and then linked as the active consul
binary. You can switch the active binary by running the same command again with a different version.

To see the versions you've already installed, you can run this command:

```
$ hcb consul list
  1.7.3
  1.8.4
  1.8.4+ent
  1.8.5
  1.8.5+ent
  1.9.4
* 1.9.4+ent
```

You can see all available versions by running this command:

```
hcb consul list-remote
```

The following HashiCorp applications are supported:

* Consul
* Terraform
* Nomad
* Vault