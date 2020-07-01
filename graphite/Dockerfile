ARG tag=latest
FROM graphiteapp/graphite-statsd:$tag

ARG paths='/opt /var/log /etc/collectd /etc/logrotate.d /etc/nginx /etc/redis /etc/run_once /etc/service /var/lib /usr/sbin /run/nginx.pid /var/tmp'
RUN touch /run/nginx.pid && \
    mkdir -p /var/tmp && \
    chgrp -R 0 ${paths} && \
    chmod -R g=u ${paths}
