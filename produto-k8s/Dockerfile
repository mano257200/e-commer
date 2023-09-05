# Use the official Python 3.7.10 Alpine Linux image as the base image
FROM python:3.7.10-alpine

# Install pipenv globally
RUN pip install pipenv

# Create and set the working directory for the app
WORKDIR /app

# Copy the Pipfile and Pipfile.lock to the container
COPY Pipfile Pipfile.lock /app/

# Install Flask and Marshmallow dependencies using pipenv
RUN pipenv install --deploy --ignore-pipfile

# Copy the rest of your application code to the container
COPY . /app/

# Make the bootstrap script executable
RUN chmod +x /app/produto/bootstrap.sh

# Expose port 8080 for the Flask app
EXPOSE 8080

# Set the entry point for the container
CMD ["/app/produto/bootstrap.sh"]
