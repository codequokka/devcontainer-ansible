FROM python:3.11.4

ARG USER_NAME=vscode
ARG WORK_DIR=/workspace

RUN apt update && \
    apt install -y iputils-ping

COPY ./requirements*.txt /tmp
RUN pip install --no-cache-dir -r /tmp/requirements.txt && \
    pip install --no-cache-dir -r /tmp/requirements-dev.txt

RUN useradd -ms /bin/bash ${USER_NAME}
USER ${USER_NAME}

WORKDIR ${WORK_DIR}
