FROM python:3.10.0-slim

COPY . /app
WORKDIR /app

#including venv at /opt directory
RUN python3 -m venv /opt/venv
RUN /opt/venv/bin/pip install pip --upgrade && \
    /opt/venv/bin/pip install -r requirements.txt && \
    #chmod +x makes entrypoint.sh executable
    chmod +x entrypoint.sh  

CMD ["/app/entrypoint.sh"]