FROM java:8-jre-alpine

ENV TRANQUILITY_VERSION=0.8.4 \
    PATH=/srv/tranquility/bin:$PATH

RUN apk add --no-cache bash && \
    apk add --no-cache --virtual .install-deps curl && \
    curl -L https://github.com/jessynt/tranquility/releases/download/v${TRANQUILITY_VERSION}/tranquility-distribution-${TRANQUILITY_VERSION}.tgz | tar zx -C /srv && \
    mv /srv/tranquility-distribution-${TRANQUILITY_VERSION} /srv/tranquility && \
    apk del --purge .install-deps

VOLUME ["/srv/tranquility/conf"]

ENTRYPOINT ["tranquility"]
