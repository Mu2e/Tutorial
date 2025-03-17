# Accessing EAF

EAF is entirely web-based at [analytics-hub.fnal.gov](https://analytics-hub.fnal.gov). To access EAF from outside of the FNAL network, you will need either:

- A Fermilab VPN connection; or
- A configured proxy. 

An addition, you will need an active services account.

## Setting up a Firefox proxy (SCD recommended method)

1. Ensure you have a valid kerberos ticket:
   ```bash
   klist  # Check ticket
   kinit <username>@FNAL.GOV  # Create new ticket
   ```

2. Start an SSH tunnel:
   ```bash
   ssh -f -N -D 9999 <username>@mu2egpvm01.fnal.gov # Start tunnel
   ```

3. Configure Firefox:

   - Enter `about:config` in the address bar
   - Modify the following parameters:

   | Parameter | Value |
   |-----------|-------|
   | network.proxy.socks | 127.0.0.1 |
   | network.proxy.socks_port | 9999 |
   | network.proxy.socks_remote_dns | true |
   | network.proxy.type | 1 |

To disable the proxy, reset `network.proxy.type` to its default value.

## Navigation

- Previous: [Overview](01-Introduction.md)
- Next: [Starting an EAF Server](03-StartingAServer.md)
- [Back to Main](../README.md)