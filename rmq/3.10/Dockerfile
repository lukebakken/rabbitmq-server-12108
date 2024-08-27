FROM rabbitmq:3.10-management

COPY --chown=rabbitmq:rabbitmq enabled_plugins /etc/rabbitmq/
COPY --chown=rabbitmq:rabbitmq rabbitmq.conf /etc/rabbitmq/rabbitmq.conf
COPY --chown=rabbitmq:rabbitmq definitions.json /etc/rabbitmq/definitions.json

EXPOSE 4369 5672 15672 15692 25672 35672-35682
