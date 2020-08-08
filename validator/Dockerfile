FROM ubuntu:18.04

RUN apt update && apt install -y wget
RUN /bin/bash -c 'wget https://github.com/prysmaticlabs/prysm/releases/download/v1.0.0-alpha.18/slasher-v1.0.0-alpha.18-linux-arm64'
RUN mv slasher-v1.0.0-alpha.18-linux-arm64 prysm-slasher && chmod +x prysm-slasher
ENTRYPOINT ["./prysm-slasher"] 