# 🐳 Docker Command Cheat Sheet

Docker simplifies container management for developers. Below is a **fun and easy guide** to the most useful Docker commands you'll need. Let's start building and managing containers like a pro! 🚀

---

## 🛠️ **Docker Basics**

1. **Run an Ubuntu Container Interactively**  
   ```bash
   docker run -it ubuntu
   ```
   *🐧 Launches an Ubuntu container in interactive mode.*

2. **List All Docker Images**  
   ```bash
   docker images
   ```
   *📦 Displays all images available locally.*

3. **Access a Running Container's Shell**  
   ```bash
   docker exec -it <container_name> bash
   ```
   *🔑 Opens a Bash shell inside a running container.*

4. **Run a Command Inside a Running Container**  
   ```bash
   docker exec <container_name> ls
   ```
   *📜 Executes the `ls` command inside the specified container.*

---

## 🌐 **Port Exposure**

5. **Run a Container and Expose Ports**  
   ```bash
   docker run -it -p 1025:1025 <image_name>
   ```
   *📡 Maps port 1025 on the host to port 1025 in the container.*

---

## 🧱 **Building and Managing Images**

6. **Build an Image from a Dockerfile**  
   ```bash
   docker build -t simplemessenger <path>
   ```
   *🔨 Builds an image tagged as `simplemessenger` from the specified path.*

7. **Remove an Image**  
   ```bash
   docker rmi <image_name_or_id>
   ```
   *🚮 Deletes an unwanted image from your local repository.*

---

## 📋 **Docker Compose**

8. **Start Services Defined in `docker-compose.yml`**  
   ```bash
   docker compose up -d
   ```
   *🚀 Launches services in detached mode.*

9. **Stop and Remove Docker Compose Services**  
   ```bash
   docker compose down
   ```
   *💔 Stops services and cleans up containers, networks, and volumes.*

---

## 🌉 **Docker Networks**

10. **Run a Container on the Host Network**  
    ```bash
    docker run -it --network=host <image_name>
    ```
    *🌍 Shares the host's network stack.*

11. **Run a Container on the Default Bridge Network**  
    ```bash
    docker run -it --network=bridge <image_name>
    ```
    *🌐 Uses Docker’s default bridge network.*

12. **Run a Container Without a Network**  
    ```bash
    docker run -it --network=none <image_name>
    ```
    *🚫 Launches the container with no network connection.*

13. **Create a Custom Bridge Network**  
    ```bash
    docker network create -d bridge <network_name>
    ```
    *🔗 Sets up a new isolated bridge network.*

---

## 📂 **Additional Useful Commands**

14. **List Running Containers**  
    ```bash
    docker ps
    ```
    *🟢 Displays currently running containers.*

15. **List All Containers (Including Stopped)**  
    ```bash
    docker ps -a
    ```
    *📜 Lists all containers, active or stopped.*

16. **Stop a Container**  
    ```bash
    docker stop <container_name_or_id>
    ```
    *🛑 Stops a running container.*

17. **Remove a Container**  
    ```bash
    docker rm <container_name_or_id>
    ```
    *🚮 Deletes a stopped container.*

18. **Check Logs of a Container**  
    ```bash
    docker logs <container_name_or_id>
    ```
    *📝 Displays logs for troubleshooting or monitoring.*

19. **Copy Files To/From a Container**  
    ```bash
    docker cp <source_path> <container_name_or_id>:<destination_path>
    docker cp <container_name_or_id>:<source_path> <destination_path>
    ```
    *📤📥 Transfers files between your host and container.*

20. **Prune Unused Docker Resources**  
    ```bash
    docker system prune
    ```
    *🧹 Cleans up unused containers, networks, and images.*

21. **Inspect a Container or Image**  
    ```bash
    docker inspect <container_name_or_id>
    ```
    *🔍 Provides detailed information about containers or images.*

22. **Start a Stopped Container**  
    ```bash
    docker start <container_name_or_id>
    ```
    *🔄 Revives a previously stopped container.*

23. **Attach to a Running Container**  
    ```bash
    docker attach <container_name_or_id>
    ```
    *👀 Connects to a running container’s input/output streams.*

24. **Tag an Image for a Repository**  
    ```bash
    docker tag <image_name> <repository_name>:<tag>
    ```
    *🏷️ Prepares an image for pushing to a repository.*

25. **Push an Image to Docker Hub**  
    ```bash
    docker push <repository_name>:<tag>
    ```
    *🌐 Uploads a tagged image to Docker Hub.*

---

## 🧹 **Pro Tip: Cleaning Up**

Keep your system tidy with this command:  
```bash
docker system prune
```
*✨ Cleans up all unused containers, images, and networks.*

---

## 🎉 **That’s It!**

This cheat sheet is your go-to guide for all the essential Docker commands. Save it, share it, and keep experimenting. With Docker, the possibilities are endless! 🐳✨  

--- 