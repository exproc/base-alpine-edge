FROM alpine:edge
RUN mkdir -pv /etc/supervisor.d
RUN apk add -U tzdata bash supervisor 
ENV TZ=America/New_York
RUN cp /usr/share/zoneinfo/America/New_York /etc/localtime 
RUN ls -la /etc/ 
COPY  src/etc/supervisor/  /etc/
RUN ls -la /etc/supervisor.d/
EXPOSE 80 443 69/udp 69/tcp
CMD ["/usr/bin/supervisord",  "-c", "/etc/supervisord.conf"]

