FROM python:3.11.0-slim-bullseye@sha256:f492c171af4e18af1be8b3bd2c719895b5d5cd0197d2e9d5c3cfc183f3d28b0f

ADD requirements.txt /tmp/flask-requirements.txt
RUN pip3 install -qr /tmp/flask-requirements.txt
RUN mkdir /code

ENTRYPOINT ["python3", "/code/service.py"]
