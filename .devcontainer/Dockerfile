FROM mcr.microsoft.com/vscode/devcontainers/base:0-buster

ENV DENO_VERSION=v1.6.3
ENV DENO_INSTALL=/deno

RUN mkdir -p /deno \
    && curl -fsSL https://deno.land/x/install/install.sh -o install-deno.sh \
    && sh install-deno.sh ${DENO_VERSION} \
    && chown -R vscode /deno \
    && chmod -R 777 /deno \
    && rm install-deno.sh

ENV PATH=${DENO_INSTALL}/bin:${PATH} \
    DENO_DIR=${DENO_INSTALL}/.cache/deno
