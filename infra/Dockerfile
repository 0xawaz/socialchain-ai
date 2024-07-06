# base image
FROM marlinorg/nitro-cli:24

RUN apk add --update docker

COPY marlin/ .

RUN rc-status --list

RUN rc-update add docker

RUN docker image build -t enclave:0xawaz .