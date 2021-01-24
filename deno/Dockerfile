FROM registry.access.redhat.com/ubi8/ubi

RUN dnf install -y curl unzip
RUN useradd deno

USER deno
WORKDIR /home/deno

RUN curl -fsSL https://deno.land/x/install/install.sh | sh
ENV PATH="/home/deno/.deno/bin:$PATH"

CMD ["deno"]
