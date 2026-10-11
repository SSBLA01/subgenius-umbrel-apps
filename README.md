# SubGenius Umbrel App Store

Community app store for umbrelOS. Add this repo's URL in Umbrel: App Store > ... > Community App Stores.

## subgenius-nomadnet

Runs on the Umbrel host network:

- **node**: NomadNet in daemon mode serving the SubGenius BBS (DoBBS) pages. Owns the Reticulum shared instance, the RNode (LoRa) on `/dev/ttyUSB0`, and the internet relay links. With `enable_transport = Yes` in the Reticulum config it routes between local LoRa users and the wider network.
- **web**: the NomadNet text browser served in a web page by ttyd on port 7681. Login user `umbrel`, password shown by Umbrel for the app.

Data stays on the host and is not in this repo:

- `/home/umbrel/.nomadnetwork` - BBS pages, data and node identity
- `/home/umbrel/.reticulum` - Reticulum config (interfaces)
- `/home/umbrel/.nomadnet-client` - browser client identity

The RNode must be plugged in for the node to start.
