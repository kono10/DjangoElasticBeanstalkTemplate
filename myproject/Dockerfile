FROM python:3.6
# TODO add volumes instead
WORKDIR /usr/src/app
COPY requirements.txt ./
RUN pip install -r requirements.txt
ENV DJANGO_ENV=PROD
# TODO update this
ENV SECRET_KEY=test_key123
COPY . .

CMD ["gunicorn", "--bind"," 0.0.0.0:8000", "--workers=4", "myproject.wsgi:application"]
