# Installing Redis

This file contains steps to install redis-cli on ubuntu system.

## Installation Steps

### On Linux

1. **Install prerequisites:**:

   ```bash
   sudo apt-get install lsb-release curl gpg
   ```

   These are used to fetch the Redis official GPG key and add the official Redis repository to your sources list.

2. **Download and install Redis GPG key:**:

   ```bash
   curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg

   sudo chmod 644 /usr/share/keyrings/redis-archive-keyring.gpg
   ```

   These steps add a trusted GPG key to authenticate the Redis package from the official Redis

3. **Enable and start the Redis service**:
   ```bash
   echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list
   ```
   This step adds the Redis official package repository to your system's sources list so that you can install the latest version of Redis.
4. **Update and install Redis:**:

   ```bash
   sudo apt-get update
   sudo apt-get install redis
   ```

5. **Configure Redis to start on boot (optional): To ensure Redis starts automatically when the server restarts, run:**

   ```bash
   sudo systemctl enable redis
   ```

6. **Test Redis: You can test if Redis is working properly by using the Redis CLI:**

   ```bash
   redis-cli ping

   Output: PONG
   ```

---

For more details, refer to the [official Redis documentation](https://redis.io/docs/).
