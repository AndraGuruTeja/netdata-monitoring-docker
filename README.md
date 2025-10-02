#  Netdata Monitoring with Docker

This repository demonstrates how to set up real-time system and application monitoring using *Netdata* inside a Docker container.

##  Dashboard

After setup, access the Netdata dashboard at:
[http://localhost:19999](http://localhost:19999)

##  Setup & Usage

### 1. Start Netdata Container

```sh
docker run -d --name=netdata \
  -p 19999:19999 \
  --cap-add=sys_ptrace \
  --security-opt apparmor=unconfined \
  netdata/netdata
```


### 2. Verify Container is Running

```sh
docker ps
```

### 3. Access the Dashboard

Open your browser and go to:
[http://localhost:19999]

### 4. List Netdata Logs Inside the Container

```sh
docker exec -it netdata ls /var/log/netdata
```

### 5. Stop and Remove the Container

```sh
docker stop netdata
docker rm netdata
```

## Deliverables

- Screenshot of Netdata dashboard (showing CPU, RAM, Disk, Network).
- Screenshot of logs directory (/var/log/netdata).