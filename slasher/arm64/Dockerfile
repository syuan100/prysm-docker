FROM ubuntu:18.04

RUN apt update && apt install -y wget && apt install -y curl && apt install -y jq
RUN /bin/bash -c "echo $(curl -H 'Accept: application/vnd.github.v3+json' https://api.github.com/repos/prysmaticlabs/prysm/releases/latest | jq -c '.assets[] | select(.name|test("(^slasher)(.*)(arm64$)"))' | jq '.browser_download_url') | xargs wget -O prysm-slasher"
RUN chmod +x prysm-slasher
ENTRYPOINT ["./prysm-slasher"]
