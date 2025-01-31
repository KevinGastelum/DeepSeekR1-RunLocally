# Tutorial: Running Deepseek R1 Locally on Your Computer

## Downloading and Running Deepseek R1 Model

### Step 1: Download and Install Ollama
Ollama is an engine that allows you to run large language models (LLMs) such as Deepseek R1 on your local machine.

1. Download Ollama from the [Ollama Download Page](https://ollama.com/download).
2. Follow the installation instructions specific to your operating system.

### Step 2: Run the Model Using Ollama
To start the Deepseek R1 model, open your terminal:

- **MacOS**: Open Terminal
- **Windows**: Open Command Prompt (CMD)

You have the option to choose from multiple model versions based on size. The 7B model (4.7GB) is recommended for most home computers. Run the following command:

```bash
ollama run deepseek-r1:7b
```

For other model versions, please refer to the [Deepseek R1 Documentation](https://api-docs.deepseek.com/).

### Step 3: Wait for Ollama to Download & Install the Model
Ollama will download and set up the model, which may take some time depending on your internet speed.

### Step 4: Use the Model via Terminal
Once the installation is complete, you can start interacting with Deepseek R1 through the terminal. If you prefer a web user interface (UI) similar to ChatGPT, follow the optional steps below.

## Optional: Setting Up a Web UI for Deepseek R1

### Step 1: Install Docker
To set up a web UI for Deepseek R1, you'll first need Docker.

1. Go to the [Docker Download Page](https://www.docker.com/products/docker-desktop) and select your operating system to install Docker.
2. Sign up for a Docker account and ensure you select Docker Personal (not Business).

### Step 2: Run Open WebUI Using Docker
To run the Open WebUI with Docker, execute the following command in your terminal:

```bash
docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
```

This command sets up the web-based interface for Deepseek R1.

### Step 3: Access and Configure Open WebUI
1. Wait approximately 2-3 minutes for the Open WebUI to start.
2. Open your web browser and navigate to `localhost:8080`.
3. Create an admin account when prompted.

### Step 4: Use Deepseek R1 via Open WebUI
You can now chat with Deepseek R1 through a ChatGPT-like interface provided by the Open WebUI!

## Restarting the Model & UI After a Computer Restart
If you restart your computer, follow these steps to get the model and UI running again:

1. Open your terminal and execute:
   ```bash
   ollama run deepseek-r1:7b
   ```
2. Open the Docker application and start the Open WebUI container.
3. Launch your browser and visit `localhost:8080`.
4. Enjoy using Deepseek R1 locally on your computer!

### Tip
If you're interested in using a different model version, check out the [Deepseek R1 Library]([https://deepseek.ai/models](https://api-docs.deepseek.com/quick_start/pricing)) for available options.

Now you have Deepseek R1 running locally with a web UI!
