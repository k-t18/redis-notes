# Configuring Redis with Node.js

## Prerequisites

- Node.js installed
- Redis server installed and running

## Installation

1. Install the `redis` package using npm:

   ```bash
   npm install redis
   ```

## Basic Usage

1. Require the `redis` package and create a redis instance:

   ```javacript
   import redis from "redis";
   const redisHost: any = process.env.NEXT_REDIS_HOST || '127.0.0.1';
   const redisPort: any = process.env.NEXT_REDIS_PORT || 6379;
   const redisServer = redis.createClient({
      socket: {
         host: redisHost,
         port: redisPort,
      },
   });
   ```
