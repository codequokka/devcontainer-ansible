FROM python:3.11.4

COPY ./requirements.txt /tmp/

RUN apt update && \
    apt install -y iputils-ping && \
    pip install --no-cache-dir -r /tmp/requirements.txt

RUN useradd -ms /bin/bash vscode

WORKDIR /workspace

USER vscode
