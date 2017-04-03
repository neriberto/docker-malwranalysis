FROM alpine

RUN apk add --no-cache libmagic
RUN apk add --no-cache git
RUN apk add --no-cache python
RUN apk add --no-cache py-pip
RUN apk add --no-cache py-lxml

RUN git clone https://github.com/neriberto/hg.git
WORKDIR /hg
RUN git checkout unstable
RUN pip install -r requirements.txt
RUN sed -i 's/localhost/viper-api/' conf/hg.conf

CMD python app.py
