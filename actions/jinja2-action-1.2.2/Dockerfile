FROM python:3.11

WORKDIR /app
ENTRYPOINT ["/app/entrypoint.py"]

COPY poetry.lock pyproject.toml README.md ./
RUN pip install poetry==1.8.5 \
 && poetry config virtualenvs.create false \
 && poetry install

COPY . ./
