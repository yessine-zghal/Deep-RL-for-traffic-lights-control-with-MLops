FROM ubuntu:20.04

LABEL maintainer="yessine.zghal@ensi-uma.tn"

RUN apt-get update -y
RUN apt install software-properties-common -y
RUN add-apt-repository ppa:sumo/stable -y
RUN apt-get update -y
RUN apt-get install sumo sumo-tools sumo-doc -y

COPY . /app
WORKDIR /app
RUN apt-get install python3.8 python3-pip -y

RUN pip3 install -r requirement.txt
WORKDIR /app/client_test

ENV SUMO_HOME /usr/share/sumo

ENTRYPOINT ["python3"]
CMD ["testing_main.py"]
