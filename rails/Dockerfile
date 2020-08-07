FROM hopsoft/base
MAINTAINER Nathan Hopkins <natehop@gmail.com>

# args are specified in .env and passed via docker-compose.yml
ARG ruby_version
ARG node_version

# install dependencies
RUN apt-get -y update\
 && apt-get -y upgrade\
 && apt-get -y --force-yes install postgresql-client\
 && apt-get clean

RUN asdf update

# install node
RUN asdf plugin add nodejs\
 && "$HOME/.asdf/plugins/nodejs/bin/import-release-team-keyring"\
 && asdf plugin update nodejs\
 && asdf install nodejs "$node_version"\
 && asdf global nodejs "$node_version"

# install ruby
RUN asdf plugin add ruby\
 && asdf plugin update ruby\
 && asdf install ruby "$ruby_version"\
 && asdf global ruby "$ruby_version"

RUN asdf reshim
CMD /bin/bash
