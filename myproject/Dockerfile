FROM python:3.6
# TODO add volumes instead
WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip install -r requirements.txt
COPY . .
RUN cd myproject 

CMD ["gunicorn", "--bind"," 0.0.0.0:8000", "--workers=4", "myproject.wsgi:application"]
