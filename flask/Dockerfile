#base image
ARG version=18.04
FROM ubuntu:${version}


#prerequesities

RUN  mkdir /app

RUN apt-get update -y && \
apt-get install -y python-pip python-dev curl
COPY ./* /app
WORKDIR /app
RUN pip install -r requirements.txt


#health-check

HEALTHCHECK --interval=10s  --timeout= CMD curl --fail http://localhost:5000/ || exit 1

#making the container executable
EXPOSE 5000
ENTRYPOINT ["python"]
CMD ["app.py"]