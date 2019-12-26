FROM ubuntu

USER root
RUN apt-get update && apt-get install -y curl

WORKDIR /mydir
COPY script.sh .
RUN chmod +x script.sh

ENTRYPOINT [ "/bin/bash" ]
CMD [ "./script.sh" ]