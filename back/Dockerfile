FROM python:3.11-slim-bullseye

ENV TZ=Asia/Tokyo

# Debian日本語化
RUN apt-get update && apt-get install -y locales \
    && apt-get clean -y && rm -rf /var/lib/apt/lists/* \
    && sed -i -e 's/# \(ja_JP.UTF-8\)/\1/' /etc/locale.gen \
    && locale-gen \
    && update-locale LANG=ja_JP.UTF-8

# 必要なパッケージのインストール
RUN apt-get update && apt-get install -y \
    curl \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Poetryインストール
ENV POETRY_HOME=/opt/poetry
RUN curl -sSL https://install.python-poetry.org | python3 - \
    && cd /usr/local/bin \
    && ln -s /opt/poetry/bin/poetry \
    && poetry config virtualenvs.create false

# Pythonパッケージインストール
WORKDIR /app
COPY ./app/pyproject.toml* ./app/poetry.lock* ./
RUN poetry install