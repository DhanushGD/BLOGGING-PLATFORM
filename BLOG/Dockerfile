# Step 1: Start with an official Python base image
FROM python:3.9-slim

# Set proxy environment variables

# Step 2: Set the working directory in the container
WORKDIR /app

# Step 3: Copy the current directory (including the app files) into the container
COPY . /app

# Step 4: Install the required dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Step 5: Expose the port Flask will run on (5001 in your case)
EXPOSE 5001

# Step 6: Set the environment variable to tell Flask to run in production mode
ENV FLASK_ENV=production

# Step 7: Set the environment variable FLASK_APP to point to your application file (main.py or app.py)
ENV FLASK_APP=main.py  

# Step 8: Set the command to run your application
CMD ["flask", "run", "--host", "0.0.0.0", "--port", "5001"]
