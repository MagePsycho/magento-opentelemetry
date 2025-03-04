FROM docker.io/wardenenv/php-fpm:8.1-magento2
USER root

RUN set -eux \
    && yum install epel-release -y \
    && yum install dnf -y \
    && dnf install -y php-pecl-opentelemetry \
    && dnf clean all \
    && rm -rf /var/cache/dnf

USER www-data
