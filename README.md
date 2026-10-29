# Experiment 08 — Docker images and containers

**Student:** [Your name]  
**Register number:** [Your register number]  
**Course:** Collaborative Development and DevOps

## Aim

Pull an image, run a container, inspect its port mapping and logs, then stop and remove it.

## Requirements

Docker Engine or Docker Desktop installed and running. Confirm with `docker --version`.

## Procedure

1. Pull and inspect the Nginx image:
   ```sh
   docker pull nginx:alpine
   docker image ls nginx
   ```
2. Start a web server container:
   ```sh
   docker run -d --name lab-nginx -p 8080:80 nginx:alpine
   docker ps
   ```
3. Open [http://localhost:8080](http://localhost:8080) and inspect the response. Then inspect logs and metadata:
   ```sh
   docker logs lab-nginx
   docker inspect lab-nginx
   docker ps -a
   ```
4. Stop and remove the container, then remove the image if it is no longer needed:
   ```sh
   docker stop lab-nginx
   docker rm lab-nginx
   docker rmi nginx:alpine
   ```

If the container name is already in use, inspect it with `docker ps -a` before deciding whether to remove it.

## What to record

Record the image tag, container ID, port mapping, browser result, and lifecycle commands. Use the values from your own Docker output; IDs and image digests vary.

## Result

Complete this section after running Docker locally. No Docker command has been run by this repository setup.

## Reference and attribution

The topic follows the Docker image and container lifecycle theme in [Smirk1308/DevOps_LAB_08](https://github.com/Smirk1308/DevOps_LAB_08). This guide is independently written.