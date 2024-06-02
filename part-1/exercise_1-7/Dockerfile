FROM ubuntu:22.04

# Use /usr/src/app as our workdir. The following instructions will be executed in this location.
WORKDIR /usr/src/app

COPY script.sh .

RUN chmod +x script.sh

RUN apt-get update && apt-get install -y curl

CMD ./script.sh


