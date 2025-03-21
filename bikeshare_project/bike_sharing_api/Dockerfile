# 1. Use official Python 3.12.3 slim base image
FROM python:3.12.3-slim

# 2. Set working directory inside container
WORKDIR /app

# 3. Copy and install dependencies from requirements.txt
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# 4. Copy entire project into the container
COPY . /app

# 5. Install your custom model package (.whl)
RUN pip install --no-cache-dir ./bikeshare_model-0.0.1-py3-none-any.whl

# 6. Expose a port if the app is a web service (optional)
# EXPOSE 8000

# 7. Run the app using Python
CMD ["python", "app/main.py"]
