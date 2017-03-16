FROM hashicorp/terraform:0.9.0
MAINTAINER Kazumichi Yamamoto <yamamoto.febc@gmail.com>

ENV TERRAFORM_SAKURAIOT_VERSION=0.1.0

ADD https://github.com/yamamoto-febc/terraform-provider-sakuraiot/releases/download/v${TERRAFORM_SAKURAIOT_VERSION}/terraform-provider-sakuraiot_linux-amd64.zip ./
RUN unzip terraform-provider-sakuraiot_linux-amd64.zip -d /bin
RUN rm -f terraform-provider-sakuraiot_linux-amd64.zip

VOLUME ["/work"]
WORKDIR /work

ENTRYPOINT ["/bin/terraform"]
CMD ["--help"]
