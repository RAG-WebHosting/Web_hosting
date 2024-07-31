# RAG API Documentation - Hosting /Doc sites 

This project provides a web interface for interacting with Retrieval-Augmented Generation (RAG) API pipelines. The web hosting solution utilizes Swagger UI to visualize and interact with API endpoints, facilitating the management and monitoring of RAG pipelines.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Overview

The RAG API Documentation project is designed to help developers manage and monitor RAG pipelines through a user-friendly web interface. This project leverages Swagger UI to provide an interactive documentation site that allows users to explore various API endpoints and their functionalities.

## Features

- **Interactive Documentation:** Utilize Swagger UI to explore API endpoints interactively.
- **User-Friendly Interface:** Navigate through API features such as Pipelines, Data Sources, Retrieval Settings, and more.
- **API Management:** Create, update, and delete RAG pipelines and associated components.
- **Performance Monitoring:** Access metrics and logs for comprehensive insights into pipeline performance.

## Getting Started

These instructions will guide you on how to set up the project on your local machine for development and testing purposes.

### Prerequisites

- **Git:** Version control system to clone the repository.
- **Node.js and npm:** Required to run local servers if you choose to serve the site locally.
- **Python:** Required if you use Python-based solutions.
- **Web Browser:** For accessing the Swagger UI interface.

### Installation

1. **Clone the Repository**

   Open your terminal and run the following command:

   ```bash
   git clone https://github.com/RAG-WebHosting/Web_hosting.git
   cd Web_hosting

2. **Install Dependencies**

   Unzip the Swagger UI distribution files:

   ```bash
   unzip swagger-ui-master.zip -d swagger-ui-master

3. **Configure Your Environment**

   Ensure that you have Node.js and npm installed. Install a simple HTTP server if needed:
   
   ```bash
   npm install -g http-server

### Usage

1. **Running the Local Server**

   Start the server to serve your HTML and YAML files:

   ```bash
   http-server -p 8000
   ```
   Open a web browser and navigate to http://localhost:8000/index.html to access the Swagger UI interface.
   
2. **Explore API Endpoints**

   Use the Swagger UI to interact with your RAG API. You can send requests to create, update, or delete pipelines and view the response data directly on the interface.

### Project Structure

1. `index.html`: The main HTML file that includes the Swagger UI interface and loads the spec.yaml file to display API documentation.
2. `spec.yaml`: The OpenAPI Specification file that defines the API endpoints, request/response models, and other documentation details.
3. `swagger-ui-master`: Directory containing Swagger UI files necessary for rendering the API documentation.

### Notes 

- **Ensure the `spec.yaml` file path is correctly specified in `index.html`:**

  ```html
  const ui = SwaggerUIBundle({
      url: "./spec.yaml",
      dom_id: '#swagger-ui',
      ...
  });

- **Custom Styling: You can modify the CSS in index.html to fit your design requirements.**
- **Server Options: You can use Python's built-in HTTP server instead:**
  ```bash
  python -m http.server 8000
  ```
By following these instructions, you'll have a fully functional local setup for exploring and managing RAG pipelines through a web interface.
   

