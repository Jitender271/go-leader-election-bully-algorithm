# Leader-Election-Bully-Algorithm
# Quickstart With Docker

Quickly set up and test the Bully Algorithm for leader election in distributed systems using Docker Compose. The provided Docker Compose file launches four nodes, allowing you to easily observe the cluster behavior.

Usage:
Build and run Docker Compose:

```docker-compose up --build```
Test the cluster behavior by killing nodes with Docker commands.

To add new nodes, update the hardcoded node addresses in the source code:

```// nodeAddressByID: Includes nodes currently in the cluster
var nodeAddressByID = map[string]string{
    "node-01": "node-01:6001",
    "node-02": "node-02:6002",
    "node-03": "node-03:6003",
    "node-04": "node-04:6004",
}
```
This repository focuses on demonstrating leader election using the Bully Algorithm without implementing a full-fledged service discovery mechanism.

# Quickstart without Docker
You can still execute this project without using Docker.

First, change the Node IPs. For example

```// nodeAddressByID: It includes nodes currently in cluster
var nodeAddressByID = map[string]string{
	"node-01": "node-01:6001", <--- change here to localhost:6001
	"node-02": "node-02:6002", <--- change here to localhost:6002
	"node-03": "node-03:6003", <--- change here to localhost:6003
	"node-04": "node-04:6004", <--- change here to localhost:6004
}
```
Second, you can set which node you want to run in Program arguments like

go run . node-02
