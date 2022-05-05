FROM python:3.8-slim-buster

LABEL maintainer="yessine.zghal@ensi-uma.tn"

COPY . /app
WORKDIR /app
RUN pip3 install -r requirement.txt
WORKDIR /app/app
EXPOSE 5000
ENTRYPOINT ["python3"]
CMD ["app.py"]