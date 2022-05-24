# Rust as the base image
FROM rust:1.51

# 1. Create a new empty shell project
RUN addgroup \
    --gid 1000 \
    docker

RUN adduser \
    --disabled-password \
    --gecos "" \
    --home "$(pwd)" \
    --ingroup docker \
    --no-create-home \
    --uid 1000 \
    docker


WORKDIR /app/holodeck

RUN echo "test" > file1
RUN echo "test" > file2

RUN chown -R 1000:1000 /app
USER docker

CMD ["sleep", "1000"]
