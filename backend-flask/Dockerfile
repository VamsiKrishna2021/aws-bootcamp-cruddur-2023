FROM python:3.10-slim-buster

# Inside Container
#make a new folder inside container
WORKDIR /backend-flask

# Outside Container -> Inside Container
# this comtains the Libraries want to install to run the app
COPY requirements.txt requirements.txt

# Inside Container
# Install the Python libraries used for the app
RUN pip3 install -r requirements.txt

# Outside Container -> Inside Container
# Means everthing inside the current directory
# First period . /backend flask(outside container)
# Second period . /backend flask(Inside container)
COPY . .

# Set Environment Variables(Env Vars)
# Inside Container and will set the container is running
ENV FLASK_ENV=development

EXPOSE ${PORT}

# CMD (Command)
# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]