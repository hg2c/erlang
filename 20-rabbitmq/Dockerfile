FROM elixir:1.6

RUN mix local.hex --force

RUN apt-get update \
    && apt-get install -y --no-install-recommends maven rsync zip
