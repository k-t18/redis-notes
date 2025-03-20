## Correct way to list all keys

```
KEYS *
```

#### Using the SCAN Command Instead of KEYS (Recommended for large datasets)

```
SCAN 0 or SCAN 0 MATCH * COUNT 10
```

### Check which database you're in

```
INFO keyspace
```

### Count total keys in the database

```
DBSIZE
```

### How to delete all keys from Redis DB

1. Delete All Keys in the Current Database

   ```
   FLUSHDB
   ```

2. Delete All Keys from All Databases

   ```
   FLUSHALL
   ```

3. Delete Keys Matching a Pattern (Safer Option)

   ```
   Delete Keys Matching a Pattern (Safer Option)
   ```
