FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl
RUN echo 'read website; sleep 3; curl http://$website;' > script.sh

CMD ["/bin/bash", "./script.sh"]