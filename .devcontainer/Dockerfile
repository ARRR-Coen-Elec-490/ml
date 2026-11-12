FROM mcr.microsoft.com/devcontainers/base:alpine

USER vscode

RUN apt-get update && apt-get install -y \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt /tmp/pip-tmp/

RUN pip3 --no-cache-dir install --upgrade pip \
    && pip3 --no-cache-dir install -r /tmp/pip-tmp/requirements.txt \
    && rm -rf /tmp/pip-tmp