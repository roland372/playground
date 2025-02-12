# Use the official Python image as a base
FROM python

# Set the working directory inside the container
WORKDIR /app

# Copy only requirements first (for caching purposes)
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the app code
COPY . .

# Expose port 8000 (Django’s default)
EXPOSE 8000

# Default command to run the app
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]