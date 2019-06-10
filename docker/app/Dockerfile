FROM python:3.7.3-slim-stretch

ARG MY_UID
ARG MY_GID

RUN groupadd -g ${MY_GID} user
RUN useradd -g ${MY_GID} -u ${MY_UID} -m user
USER user:user

WORKDIR /app/

COPY requirements.txt .
RUN pip install --user -r ./requirements.txt