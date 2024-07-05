FROM python:alpine3.10      
# base image 
WORKDIR /app 
# initiliazing working directory
COPY . /app
# copying the current directory to the working directory
RUN pip install -r requirements.txt
# installing the requirements present in requirements.txt
EXPOSE 5000
# exposing the port 5000 to outside world
CMD python ./launch.py
# running the launch.py file

#COPY requirements.txt /app/requirements.txt
#ENTRYPOINT ["python", "./launch.py"]
# alpine is is very small version of the linux works very good with docker

# for building
# docker build -t in28min/hello-world-python:0.0.2.RELEASE .

# for running
# docker run -p 5000:5000 -d in28min/hello-world-python:0.0.2.RELEASE