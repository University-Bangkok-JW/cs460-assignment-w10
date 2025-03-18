# Use the official Python image as the base
FROM python:3.12

# Set the working directory
WORKDIR /workspace

# Install system dependencies
RUN apt-get update && apt-get install -y \
    git \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Install Jupyter and common Python libraries
RUN pip install --no-cache-dir jupyterlab numpy pandas matplotlib seaborn scipy scikit-learn

# Expose Jupyter Notebook port
EXPOSE 8888

# Set the default command to start Jupyter Notebook
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]
