# This is RabbitMQ Tutorial

## Step 1: Setup RabbitMQ

**Docker**

```shell
docker run -d --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:4.0-management
```

**Docker Compose**

```yaml
services:
  rabbitmq:
    image: rabbitmq:4.0-management
    container_name: "rabbitmq"
    ports:
      - 5672:5672
      - 15672:15672
    volumes:
      - ~/.docker-conf/rabbitmq/data/:/var/lib/rabbitmq/
      - ~/.docker-conf/rabbitmq/log/:/var/log/rabbitmq
    networks:
      - rabbitmq

networks:
  rabbitmq:
    driver: bridge
```

```shell
docker-compose up -d
```

## Connect Web Management

Access url : http://localhost:15672

**Default Account**

- Username

  ```shell
  guest
  ```

- Password

  ```shell
  guest
  ```
