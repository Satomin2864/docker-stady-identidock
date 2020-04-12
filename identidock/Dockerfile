FROM python:3.7

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi
RUN pip3 install --upgrade pip && pip install flask && pip install uwsgi && pip install requests==2.5.1 && pip install redis==2.10.3 
WORKDIR /app
COPY app /app
COPY cmd.sh /

EXPOSE 9090 9191
USER uwsgi

CMD ["/cmd.sh"]
