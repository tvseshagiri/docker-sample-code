FROM python:3-alpine3.12
LABEL author "Seshagiri Telkapalli"
COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt
ENTRYPOINT ["python"]
CMD ["app.py"]