# Chatwoot Docker Service

This project provides a Docker setup for running Chatwoot, an open-source customer support tool that helps businesses manage customer interactions across various channels.

## Description

This repository contains Docker configurations to easily deploy Chatwoot. Chatwoot is designed to help businesses provide better customer support by centralizing communication and offering features like live chat, email support, and more.

## Services

- **Rails**: The main service that runs the Chatwoot application.
  - **Container Name**: rails
  - **Image**: chatwoot/chatwoot:latest
  - **Ports**: Exposed on port 3000
  - **Environment Variables**: 
    - NODE_ENV: production
    - RAILS_ENV: production
    - INSTALLATION_ENV: docker
  - **Health Check**: Ensures Rails is running by checking the health endpoint.

- **Sidekiq**: A background job processor for Chatwoot.
  - **Container Name**: sidekiq
  - **Image**: chatwoot/chatwoot:latest
  - **Environment Variables**: 
    - NODE_ENV: production
    - RAILS_ENV: production
    - INSTALLATION_ENV: docker
  - **Health Check**: Ensures Sidekiq is running by checking the health endpoint.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/chatwoot-docker.git
   ```

2. Navigate to the project directory:

   ```bash
   cd chatwoot-docker
   ```

3. Start the services using Docker Compose:

   ```bash
   docker-compose up -d
   ```

## Usage

- Access Chatwoot at [http://localhost:3000](http://localhost:3000) to manage customer interactions.
- Use the Chatwoot interface to set up channels, manage conversations, and provide support.

## Contributing

1. Fork the repository.
2. Create a new branch:

   ```bash
   git checkout -b feature/YourFeature
   ```

3. Make your changes and commit them:

   ```bash
   git commit -m "Add your message"
   ```

4. Push to the branch:

   ```bash
   git push origin feature/YourFeature
   ```

5. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
