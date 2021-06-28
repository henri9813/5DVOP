FROM python:2.7-stretch

MAINTAINER Henri Devigne <henri.devigne@ecole-it.com>

RUN apt-get update \
 && apt-get install --yes \
 	python-dev \
 	libsasl2-dev \
 	libldap2-dev \
 	libssl-dev \
 && rm -rf /var/lib/apt/lists

RUN pip install flask flask_httpauth flask_simpleldap python-dotenv

ADD student_age.py /student_age.py

CMD [ "python2.7", "/student_age.py" ]
VOLUME '/data'
EXPOSE '5000'
