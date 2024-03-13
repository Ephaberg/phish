# Dockerfile

# Author       : Ephaberg
# Github       : https://github.com/Ephaberg
# Telegram     : https://t.me/Ephaberg
# Email        : info@ephaberg.com
# Date         : 25-08-2021
# Main Language: Python

# Download and import main images

# Operating system
FROM debian:latest
# Main package
FROM python:3

# Author info
LABEL MAINTAINER="https://github.com/Ephaberg/phish"

# Working directory
WORKDIR /phish/
# Add files 
ADD . /phish

# Installing other packages
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install python3-pip php openssh-client -y
RUN pip3 install -r files/requirements.txt --break-system-packages
RUN apt-get clean

# Main command
CMD ["python3", "phish.py", "--noupdate"]

## Wanna run it own? Try following commands:

## "sudo docker build . -t Ephaberg/phish:latest", "sudo docker run --rm -it Ephaberg/phish:latest"

## "sudo docker pull Ephaberg/phish", "sudo docker run --rm -it Ephaberg/phish"
