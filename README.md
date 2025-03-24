# Jupyter Docker Compose

A quick and easy setup for running Jupyter notebooks in a Dockerized environment, managed using [Docker Compose](https://docs.docker.com/compose/).

## Getting Started

Start the Jupyter Notebook server:

```bash
docker compose up -d
```

After running this command, the Jupyter Notebook server should be accessible at `http://localhost:8888`.

## Usage Options

You can work with Jupyter notebooks in different ways:

1. **Connect via Browser:**
   - Open your browser and go to `http://localhost:8888`.
   - Use Jupyter Notebook's built-in interface to create and manage notebooks.

2. **Use VS Code with Jupyter Extension:**
   - Install the [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) extension in VS Code.
   - Open VS Code and go to the Jupyter extension settings.
   - Select `localhost:8888` as the Jupyter server to connect to your running instance.
   - Open and edit notebooks directly from VS Code.

## Directory Structure

- `./work`: This is the directory where you can add your Jupyter notebooks. It's mounted as a volume in the Docker container, so notebooks created and saved in the Jupyter Notebook IDE will persist here.

## Notes

The `requirements.txt` file is copied to the Docker container during the build process, and the Python dependencies listed within are installed. To add or update dependencies, modify this file, then rebuild the Docker image.
