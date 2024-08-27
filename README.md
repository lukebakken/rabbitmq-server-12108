# Users

* Username: `rabbitmq-server-12108`
* Password: `test12108`

User is an `administrator`

# Demonstration

```
git clone https://github.com/lukebakken/rabbitmq-server-12108.git
cd rabbitmq-server-12108
docker compose build --no-cache --pull
docker compose up
```

The above will do the following:

* Start a RabbitMQ 3.10 node, and import definitions, including a vhost, user, and shovel.
* Start a RabbitMQ 3.12 node, creating the same vhost and user, but no shovel

In the Management UI (http://localhost:15672), go to "Shovel Status" and it
will be running.

Go to http://localhost:15673/#/connections to see the shovel connection from
the other node.

Then, on the 3.10 node, publish messages to the `rabbitmq-server-12108` queue,
and they will be shovelled to the other node.
