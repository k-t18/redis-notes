## Connect to the Redis server:

```javascript
redisServer.on("connect", function () {
  console.log("Connected to Redis...");
});
```

## Setting and Getting Values

1. Set a value in Redis:

   ```javascript
   redisServer.set("key", "value", redis.print);
   ```

2. Get a value from Redis:
   ```javascript
   redisServer.get("key", function (err, reply) {
     if (err) throw err;
     console.log(reply);
   });
   ```

## Error Handling

1. Handle connection errors:
   ```javascript
   redisServer.on("error", function (err) {
     console.log("Error " + err);
   });
   ```

## Closing the Connection

1. Close the Redis connection:
   ```javascript
   redisServer.quit();
   ```

## Additional Resources

- [Node Redis GitHub Repository](https://github.com/NodeRedis/node-redis)
- [Redis Documentation](https://redis.io/documentation)
