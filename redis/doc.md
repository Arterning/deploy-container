docker exec -it redis /bin/bash
redis-cli

127.0.0.1:6379> config get requirepass
127.0.0.1:6379> config set requirepass xxx