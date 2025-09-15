#set base image
FROM python:3.12
#set working directory
WORKDIR /app
#copy from localsource to remote
COPY . .
#install 
RUN pip install -r requirements.txt
#open port
EXPOSE 5000
#starting command
CMD ["python3", "app.py"]


