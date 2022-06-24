FROM python:3.9.13
ENV PYTHONBUFFERED=1 \
    POETRY_VIRTUALENVS_IN_PROJECT=true

WORKDIR /src

COPY main.py /src
COPY pyproject.toml /src

RUN apt-get update && apt-get -y upgrade
RUN pip install --upgrade pip
RUN pip install poetry
RUN poetry install

ENTRYPOINT ["poetry", "run", "python", "main.py"]