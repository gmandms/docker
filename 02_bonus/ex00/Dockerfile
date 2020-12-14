FROM ubuntu

MAINTAINER sbump <sbump@student.21-school.ru>

RUN apt-get update -y && apt-get install -y cowsay && ln -s /usr/games/cowsay /usr/bin/cowsay

ENTRYPOINT ["cowsay"]
