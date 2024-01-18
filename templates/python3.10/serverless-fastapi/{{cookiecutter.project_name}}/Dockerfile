FROM public.ecr.aws/lambda/python:3.8

COPY ./requirements.txt ./requirements.txt
RUN pip install -r ./requirements.txt

# Copy all relevant app files
COPY ./app ./app

# Expose port 8000 in Docker and forward to localhost:80
EXPOSE {{cookiecutter.port_config}}  

# Run the API when container starts
CMD ["app.main.handler"]

