# docker/Dockerfile   (copy everything in this box)

# Use slim Python image to keep the container small
FROM python:3.12-slim

# All work inside /app
WORKDIR /app

# 1. Install Python dependencies
COPY docker/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# 2. Copy the homework sources (CSV files excluded to save space)
COPY homework_2 ./homework_2
COPY notebooks   ./notebooks
COPY src         ./src

# 3. Drop into bash by default (handy for grading)
CMD ["bash"]
