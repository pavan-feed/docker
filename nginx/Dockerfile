#Setting up the base image

ARG version=18.04
FROM ubuntu:${version}

#customizations

RUN apt-get update && apt-get install -y curl nginx \
&& apt-get clean \
&& rm -rf /var/lib/apt/lists/*



RUN mkdir /nginx-dir
ENV USER pavan
ENV SHELL /bin/bash
EXPOSE 80


#providing a default command
CMD ["nginx", "-g", "daemon off;"]