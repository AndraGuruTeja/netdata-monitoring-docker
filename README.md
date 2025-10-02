
Netdata Monitoring Task
Objective

Set up real-time system and application monitoring using Netdata in Docker.

Tools Required

Docker

Netdata

Steps
1. Start Netdata Container
docker run -d --name=netdata \
  -p 19999:19999 \
  --cap-add=sys_ptrace \
  --security-opt apparmor=unconfined \
  netdata/netdata

2. Verify Container
docker ps

3. Access the Dashboard
http://localhost:19999

4. Check Netdata Logs
docker exec -it netdata ls /var/log/netdata

5. Stop and Remove Container
docker stop netdata
docker rm netda