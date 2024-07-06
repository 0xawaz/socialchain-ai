# Social Chain Infrastructure

## Marlin

This build is based on [Marlin Oyster doc](https://docs.marlin.org/user-guides/oyster/instances/quickstart/build).

## Marlin Default inclave image

#### Build image

```bash
docker image build -t enclave:0xawaz .
```

#### Conversion to Enclave image

##### Install binaries

We will use marlinorg/nitro-cli docker image which has nitro-cli installed, to avoid building nitro-cli from source.

```bash
docker pull marlinorg/nitro-cli:24
```

##### Convert docker image into enclave image

```bash
# nitro-cli build-enclave --docker-uri enclave:0xawaz --output-file enclave.eif
# We prefer to use docker image we pulled

docker run -it --rm marlinorg/nitro-cli:0xawaz sh

docker run -it --rm marlinorg/nitro-cli:24 sh nitro-cli build-enclave --docker-uri enclave:0xawaz --output-file enclave.eif
```

## Social Chain Enclave image

## Social Chain Value proposition

### Infrastructure Security

#### Docker image scanning

We found a [CVE-2024-5535](https://security.alpinelinux.org/vuln/CVE-2024-5535) in the initial docker image for enclave image. We managed to fix it.

#### Infra Automation
Coming soon


