FROM elixir:1.6

RUN mix local.hex --force

RUN apt-get update \
    && apt-get install -y --no-install-recommends maven rsync unzip zip

RUN mkdir -p /opt/rabbitmq && \
    cd /opt/rabbitmq && \
    wget https://www.rabbitmq.com/releases/rabbitmq-erlang-client/v3.6.14/rabbit_common-3.6.14.ez && \
    unzip rabbit_common-3.6.14.ez && \
    ln -s rabbit_common-3.6.14 rabbit_common && \
    wget https://www.rabbitmq.com/releases/rabbitmq-erlang-client/v3.6.14/amqp_client-3.6.14.ez && \
    unzip amqp_client-3.6.14.ez && \
    ln -s amqp_client-3.6.14 amqp_client && \
    wget https://www.rabbitmq.com/releases/rabbitmq-erlang-client/v3.6.14/recon-2.3.2.ez && \
    unzip recon-2.3.2.ez && \
    ln -s recon-2.3.2 recon
