FROM maxexcloo/debian:latest
MAINTAINER Max Schaefer <max@excloo.com>
ENV DOCKER_HOST unix:///tmp/docker.sock
ENV VERSION 0.3.1
RUN wget -O - "https://www.github.com/jwilder/docker-gen/releases/download/${VERSION}/docker-gen-linux-amd64-${VERSION}.tar.gz" | tar -C /usr/local/bin -x -z
ADD haproxy.tmpl /config/data/haproxy.tmpl
ADD supervisord.conf /etc/supervisor/conf.d/docker-gen.conf
VOLUME /config/temp
