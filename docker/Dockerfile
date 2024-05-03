FROM alpine:latest
WORKDIR /priviblur

# Rust is needed for orjson
RUN apk add --no-cache git python3 py3-pip rust cargo tini && \
    addgroup -g 1000 -S priviblur && \
    adduser -u 1000 -S priviblur -G priviblur && \
    git clone --depth=1 https://github.com/syeopite/priviblur.git . && \
    pip3 install --break-system-packages -r requirements.txt && \
    pybabel compile -d locales -D priviblur && \
    git config --global --add safe.directory /priviblur

EXPOSE 8000
USER priviblur
ENTRYPOINT [ "/sbin/tini", "--"]
CMD [ "python", "-m", "src.server" ]