FROM mcr.microsoft.com/devcontainers/base:1.0.0-alpine-3.19

USER vscode

RUN apt-get update && apt-get install -y \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt /tmp/pip-tmp/

RUN pip3 --no-cache-dir install --upgrade pip \
    && pip3 --no-cache-dir install -r /tmp/pip-tmp/requirements.txt \
    && rm -rf /tmp/pip-tmp