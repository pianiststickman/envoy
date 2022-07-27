FROM python:3.10.5-slim-bullseye@sha256:26963a2f657885568bfad6a8dd9031fffbe7cc89b433b65d0fec97f9d072c386

ADD requirements.txt /tmp/flask-requirements.txt
RUN pip3 install -qr /tmp/flask-requirements.txt
RUN mkdir /code

ENTRYPOINT ["python3", "/code/service.py"]
