# Moonshot API Collection
## Overview
This repository contains a collection of API implementations for interacting with the Moonshot AI services. The APIs are organized into different folders for various functionalities such as Chat, File operations, and Others.

# Introduction to Bruno

**Bruno** is an open-source Integrated Development Environment (IDE) designed for exploring and testing APIs. It aims to revolutionize the status quo of existing API client tools like Postman with its innovative approach. Key features of Bruno include:

- **Local Storage**: Bruno stores your API collections directly in your file system using a plain text markup language called Bru.
- **Version Control Friendly**: It integrates seamlessly with Git or any version control system of your choice, facilitating collaboration and version management.
- **Completely Offline**: Bruno is an offline-first tool that values user data privacy and has no plans for cloud synchronization.
- **Multi-platform Support**: Available for Mac, Windows, and Linux, Bruno can run on a variety of operating systems.
- **Community-Driven**: It has an active open-source community that continually iterates and improves the tool.

Bruno offers a [free and open-source version](https://www.usebruno.com/downloads) as well as a [paid Golden Edition](https://www.usebruno.com/pricing) with additional features. Whether for personal use or team collaboration, Bruno is a powerful tool for managing API development and testing.

For more information about Bruno, visit the [official website](https://www.usebruno.com) or its [GitHub repository](https://github.com/usebruno/bruno).

## Environment Setup
To use the APIs, you need to set up an environment variable named `MOONSHOT_API_KEY`. This key is used for authentication and should be treated as sensitive information.

### Secrets Management
For managing secrets like the `MOONSHOT_API_KEY`, Bruno provides a feature to mark variables as `secret`. When a variable is marked as secret, Bruno manages it internally and does not write it into the environment file (`environments/local.bru`). This ensures that your sensitive data is not exposed when you check in your collection to source control.

## API Endpoints
Here's a brief overview of the APIs included in this collection:

### Chat
- **Chat Completion**: Generates a response to a user's query using a specified model.
- **Chat Completion (stream)**: Similar to Chat Completion but with streaming enabled for real-time responses.
- **List Models**: Retrieves a list of available models for chat completion.
- **Tool Use**: Executes code to perform specific tasks, such as checking if a number is prime.
- **Partial Mode**: Extracts information from a product description and outputs it in a JSON object.
- **Partial Mode (Roleplay)**: Engages in a roleplay scenario and responds in character.

### File
- **upload files**: Uploads a file to the Moonshot service.
- **list files**: Lists all the files uploaded by the user.
- **DELETE file**: Deletes a specific file identified by its ID.
- **Get file information**: Retrieves information about a specific file.
- **Get file content**: Gets the content of a specific file.

### Others
- **Calculate Token**: Estimates the number of tokens required for a given message.
- **Check balances**: Checks the user's current balance for API usage.

## Bruno Usage
To use Bruno for managing your API collection, follow these steps:

1. **Create a New Collection**: Start by creating a new collection in Bruno.
2. **Add Environment Variables**: Define your environment variables, marking the `MOONSHOT_API_KEY` as a secret.
3. **Configure Requests**: Set up each HTTP request with the appropriate URL, method, headers, body, and authentication.
4. **Use Variables**: Utilize the `{{MOONSHOT_API_KEY}}` variable in the authentication bearer token field to inject the API key securely.
5. **Export Collection**: When you're ready to share or deploy, export your collection as a file. Bruno will not include secret variables in the exported file.

## Contributing
If you'd like to contribute to this repository, please follow the standard fork-and-pull request workflow. Make sure to update the `README.md` with any new APIs or significant changes.

## License
This project is licensed under the [WTFPL] - see the `LICENSE` file for details.

## Acknowledgments
- Bruno for providing a great API management tool.
- Moonshot AI for their innovative AI services.

For more information on Bruno's secrets management and other features, visit [Bruno Docs](https://docs.usebruno.com/secrets-management/secret-variables).