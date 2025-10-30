# Use an official Python image
FROM python:3.10-alpine

# Set working directory
WORKDIR /app

# Install system dependencies needed for NLTK
RUN apk add --no-cache gcc musl-dev libffi-dev openssl-dev

# Copy files
COPY . .

# Install Python packages
RUN pip install --no-cache-dir -r requirment.txt

# Download NLTK data during build
RUN python -m nltk.downloader vader_lexicon

# Run the script
CMD ["python", "main.py"]
