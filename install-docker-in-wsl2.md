# Docker in WSL2

To install Docker in WSL2, follow these steps:

1. **Enable WSL2 Backend for Docker Desktop:**

   - Download and install [Docker Desktop](https://www.docker.com/products/docker-desktop).
   - During installation, ensure **"Use the WSL2 based engine"** is enabled.
   - After installation, go to Docker Desktop settings and set **WSL integration** to **enabled**.

2. **Check WSL Integration:**
   Open **PowerShell** and run:

   ```powershell
   wsl --list --verbose
   ```

   Ensure your distribution is running under **WSL version 2**.

3. **Test Docker in WSL2:**
   Open **WSL2 (Ubuntu or other Linux distro)** and run:

   ```bash
   docker --version
   ```

   Then verify Docker is working:

   ```bash
   docker run hello-world
   ```

Now, Docker should be working inside WSL2! 🎉
