# Use docker to run neo4j database

[docker-compose 的範例](https://github.com/yuanyu90221/neo4j-docker-compose)

```yaml
version: '3'

services:
  neo4j:
    image: neo4j:latest
    container_name: 'neo4j'
    restart: always  
    volumes:
      - ./data/db:/data/db
    ports:
      - 7474:7474
      - 7687:7687
    command: neo4j
```

設定使用最新的 neo4j image

開啟 7474 這個開放給瀏覽器介面操作的 port

開啟 7687 這個開放給一般 client 連線 的 port
