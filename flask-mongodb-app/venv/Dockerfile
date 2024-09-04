FROM python:3.11
WORKDIR /app
COPY . /app/
RUN pip install -r /app/requirements.txt
EXPOSE 5000
ENV FLASK_APP=app.py
ENV FLASK_ENV=deployment
ENV $(cat .env | xargs)
CMD ["python","app.py"]