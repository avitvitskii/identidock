FROM python:3.9

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi
WORKDIR /app
COPY app /app
COPY cmd.sh /
COPY requirements.txt /app/requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 9090 9191
USER uwsgi

CMD ["/cmd.sh"]
