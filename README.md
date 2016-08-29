# buUuk stack
This repo is an automatic build for dockerhub repo [paulylz/ubuntu_ruby_mysql/](https://hub.docker.com/r/paulylz/ubuntu_ruby_mysql/).

This is the standard buUuk stack of Linux and Ruby, with apt-get drivers for connecting to a MySQL server and practical tools such as wget, curl and vim. This container is built with running things using the Docker one process per container paradigm. As such, it is ideal to run Thin or Puma in the container while reverse proxying with nginx either from another container, or from the docker host.

Contrary to [samchandra/ubuntu_ruby_mysql](https://hub.docker.com/r/samchandra/ubuntu_ruby_mysql/) which uses phusion/baseimage and the fat container paradigm, where crontab, redis and sidekiq are meant to be loaded into a single container, with this setup, I expect to have another two separate containers for sidekiq and cron (also using this image and app source code), and one more still for redis ([redis:alpine](https://hub.docker.com/_/redis/)).

### Changelog
- 29/8/2016 Upgrade to Ruby 2.3.1

