# SSH Via Wireguard

This action enables SSH access to a remote secured host via a WireGuard tunnel. The action is intended to be used with self-hosted runners on GitHub Actions.

## Disclaimer

This action is based on omahn/wireguard-ssh-github-action and appleboy/ssh-action. The original action from omahn is not maintained anymor and needs better UX. The original action from appleboy does not include wireguard support.

## Description

This action will create a WireGuard tunnel to a remote host, and then use that tunnel to create an SSH connection to the remote host. The SSH connection will be forwarded to the local machine, and the action will wait for the connection to be closed before terminating.

## Usage

```yaml
- uses: niwee-productions/actions-ssh-wireguard@beta
  with:
    # Required: The SSH user to connect as.
    user: ""
    # Required: The SSH host to connect to.
    host: ""
    # Required: The SSH port to connect to.
    port: ""
    # Required: The SSH private key to use for authentication.
    key: ""
    # Required: The WireGuard configuration to use for the tunnel.
    conf: ""
    # Required: The script to run on the remote host after the tunnel is established.
    script: ""
```
