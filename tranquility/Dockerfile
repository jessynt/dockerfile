FROM java:8-jre-alpine

ENV TRANQUILITY_VERSION=0.8.3 \
    PATH=/srv/tranquility/bin:$PATH

RUN apk add --no-cache bash && \
    apk add --no-cache --virtual .install-deps curl && \
    curl -L http://static.druid.io/tranquility/releases/tranquility-distribution-${TRANQUILITY_VERSION}.tgz | tar zx -C /srv && \
    mv /srv/tranquility-distribution-${TRANQUILITY_VERSION} /srv/tranquility && \
    apk del --purge .install-deps

VOLUME ["/srv/tranquility/conf"]

ENTRYPOINT ["tranquility"]
