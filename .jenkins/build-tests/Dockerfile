FROM python:3.6.6-stretch

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
RUN pip install -q pytest==3.9.3 awscli pytest-xdist pytest-html feather-format lxml openpyxl xlrd numpy matplotlib sqlalchemy

COPY . .
RUN pip install -e .

ENTRYPOINT ["bash", ".jenkins/build-tests/run_test.sh"]
