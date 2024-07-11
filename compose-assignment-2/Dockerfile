# create your custom drupal image here, based of official drupal
FROM drupal:9

ENV http_proxy http://tudas-proxy.rd.hu.t-internal.com:3128
ENV https_proxy http://tudas-proxy.rd.hu.t-internal.com:3128

RUN apt-get update && apt-get install -y git \
    && rm -rf /var/lib/apt/lists/* \
    && cd /var/www/html/themes \
    && git clone --branch 8.x-4.x --single-branch --depth 1 https://git.drupalcode.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap \
    && cd /var/www/html
