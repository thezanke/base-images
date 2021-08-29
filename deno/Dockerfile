FROM registry.access.redhat.com/ubi8/ubi-minimal

LABEL org.opencontainers.image.source https://github.com/thezanke/base-images

RUN microdnf install -y shadow-utils curl unzip && microdnf clean all
RUN useradd deno

USER deno
WORKDIR /home/deno

ENV DENO_DIR=/home/deno/.cache
RUN curl -fsSL https://deno.land/x/install/install.sh | sh
ENV PATH="/home/deno/.deno/bin:$PATH"

CMD ["deno"]
