FROM python:3
ENV PYTHONUNBUFFERED 1
RUN mkdir /backend
WORKDIR /backend
ADD requirements.txt /backend/
COPY start.sh /start.sh

RUN pip install -r requirements.txt
ADD . /backend
RUN ls -all
CMD ["/start.sh"]
