FROM python:3.11.4-alpine

# workdir in the container
WORKDIR /usr/src/app/ 

# prevent Python from writing .pyc files
ENV PYTHONDONTWRITEBYTECODE = 1

# ensure Python output is sent directly to the terminal without buffering
ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip
# copy from where to!
COPY ./requirements.txt /usr/src/app/requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# copy everything from here to container
COPY . /usr/src/app/