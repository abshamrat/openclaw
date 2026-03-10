This video provides a step-by-step guide on how to install and set up OpenClaw using an Alpine Docker image on an Ubuntu Linux system.

1. System Preparation
Access Root User: Open the Ubuntu terminal and switch to the root user using sudo su to ensure you have the necessary permissions for installation [00:13].

Update System: Run commands to update the system repositories and all installed packages to ensure compatibility [00:26].

2. Install Docker
Automatic Installation: Use the official Docker installation script to install both Docker and Docker Compose automatically [00:38].

3. Download and Configure OpenClaw
Clone Repository: Clone the OpenClaw source code from GitHub. The video demonstrates cloning a specific tag, though you can also use the main branch [00:53].

Modify Docker Image: Open the docker-compose.yml file and update the openlow_image variable to use the existing alfane/openclaw image. This avoids the need to build a new image from scratch [01:26].

Environment Setup: Create a hidden .env file in the project directory and add the required directory variables for the config and workspace [02:04].

4. Launch the Container
Start OpenClaw: Run the docker-compose up -d command to create and start the OpenClaw gateway container [02:23].

Permissions Fix: Adjust the ownership of the /root/.openclaw directory to prevent permission issues [02:56].

5. Onboarding Wizard
Run Onboarding: Use the command docker-compose run onboard to start the setup wizard [03:16].

API Configuration: Select your API provider (e.g., Google Gemini). You will need to generate and paste an API key from the Google AI Studio [03:32].

Channel Setup (Telegram):

Create a new bot using BotFather on Telegram to get a bot token [04:29].

Paste the token into the onboarding wizard to link the bot [05:03].

6. Final Pairing and Testing
Pairing: To authorize your Telegram account, run the pairing approval command through Docker Compose [05:47].

Verification: Send a message to your new Telegram bot. In the video, the user tests the setup by asking for the "hostname," which correctly returns the Docker container ID [06:05].

For more details, you can watch the full video here: https://www.youtube.com/watch?v=Zqnzg6W9rjY
