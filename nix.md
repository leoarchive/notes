
## Use DHCP

Modify /etc/nixos/configuration.nix, ensure the NIC is using DHCP, and then run nixos-rebuild switch should get a static internal IP now.

```
networking.interfaces.<your NIC>.useDHCP = true;
```

use `lsblk`, start with enp, same ip (inet)

## Enable SSH
The following code enable SSH for NixOS.

```
users.users.<user name> = {
  # ...
  openssh.authorizedKeys.keys = [
    "<your local public key>"
  ];
}
services.openssh.enable = true;
```
