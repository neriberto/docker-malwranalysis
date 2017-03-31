FROM alpine

RUN apk add --no-cache clamav clamav-libunrar
COPY conf /etc/clamav/
RUN mkdir /run/clamav
RUN chown -R clamav:clamav /run/clamav
RUN freshclam
RUN freshclam -d -c 6

CMD ["clamd"]
