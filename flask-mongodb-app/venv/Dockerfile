FROM python:3.11
WORKDIR /app
COPY . /app/
RUN pip install -r /app/requirements.txt
RUN pip install "pymongo[srv]" 
EXPOSE 5000
ENV FLASK_APP=app.py
ENV FLASK_ENV=deployment
CMD ["python","app.py"]