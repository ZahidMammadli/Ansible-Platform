FROM apache/superset:5.0.0

USER root

RUN apt-get update && apt-get install -y \
    build-essential \
    libpq-dev \
 && rm -rf /var/lib/apt/lists/*

# Install psycopg2 DIRECTLY into Superset’s pythonpath
RUN pip install --no-cache-dir psycopg2-binary --target=/app/pythonpath

USER superset
