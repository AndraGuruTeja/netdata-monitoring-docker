# 🖥️ Netdata Monitoring with Docker

This repository demonstrates how to set up real-time system and application monitoring using **Netdata** inside a Docker container.

## 🌐 Dashboard

After setup, access the Netdata dashboard here:
[http://localhost:19999](http://localhost:19999)

## 📁 Repository

[github.com/<your-username>/netdata-monitoring-docker](https://github.com/<your-username>/netdata-monitoring-docker)

## 🚀 Setup & Usage

1. **Start Netdata container**

docker run -d --name=netdata \
  -p 19999:19999 \
  --cap-add=sys_ptrace \
  --security-opt apparmor=unconfined \
  netdata/netdata 

2. **Verify container**

docker ps

3. **Access the dashboard**

Open browser and go to:
http://localhost:19999

4. **List Netdata logs inside the container**

docker exec -it netdata ls /var/log/netdata

5. **Stop and remove the containers**

docker stop netdata
docker rm netdata

6. **Deliverables**

Screenshot of Netdata dashboard (showing CPU, RAM, Disk, Network).

Screenshot of logs directory (/var/log/netdata).














echo "# netdata-monitoring-docker" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/AndraGuruTeja/netdata-monitoring-docker.git
git push -u origin main