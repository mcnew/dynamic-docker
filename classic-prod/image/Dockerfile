FROM ubuntu AS builder

RUN apt update \
 && apt install -y unzip

ADD https://github.com/mcnew/dynamic-templates/archive/refs/heads/main.zip /tmp/

RUN mkdir /usr/app \
 && cd /usr/app \
 && unzip /tmp/main.zip

FROM classic

COPY --from=builder /usr/app/dynamic-templates-main $TEMPLATES
