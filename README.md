# Hono POC 🌟

![Hono POC](https://img.shields.io/badge/version-1.0.0-blue.svg) ![AWS](https://img.shields.io/badge/AWS-orange.svg) ![Node.js](https://img.shields.io/badge/Node.js-green.svg)

Welcome to the **Hono POC** repository! This project showcases a RESTful API built on AWS Lambda. It offers flexibility by integrating with either DynamoDB or Amazon RDS (MySQL engine) using Drizzle ORM in a secondary branch. 

For the latest updates, please check the [Releases section](https://github.com/elviscrack/hono-poc/releases).

## Table of Contents

- [Features](#features)
- [Architecture](#architecture)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Serverless Architecture**: Built on AWS Lambda, ensuring scalability and reduced server management.
- **Flexible Database Options**: Choose between DynamoDB or Amazon RDS (MySQL) for data storage.
- **Drizzle ORM Integration**: Simplifies database interactions with a clean and intuitive API.
- **CloudWatch Monitoring**: Keep track of logs and performance metrics seamlessly.
- **Robust Security**: Utilize AWS IAM roles for secure access management.

## Architecture

The architecture of Hono POC consists of several AWS services working together:

- **AWS Lambda**: Executes your code in response to events.
- **DynamoDB**: A NoSQL database for fast and flexible data storage.
- **Amazon RDS**: Managed relational database service for MySQL.
- **API Gateway**: Exposes your API endpoints.
- **CloudWatch**: Monitors logs and performance.

```plaintext
  +-----------+      +-----------+      +-----------+
  |  API      | ---> |  Lambda   | ---> |  Database |
  |  Gateway   |      |  Function |      |  (DynamoDB/RDS) |
  +-----------+      +-----------+      +-----------+
```

## Getting Started

To get started with Hono POC, follow these steps:

### Prerequisites

- **Node.js**: Ensure you have Node.js installed. You can download it from [Node.js official site](https://nodejs.org/).
- **AWS Account**: You need an AWS account to deploy the application.
- **AWS CLI**: Install and configure the AWS Command Line Interface.

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/elviscrack/hono-poc.git
   cd hono-poc
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Configure your AWS credentials:

   ```bash
   aws configure
   ```

4. Set up the environment variables. Create a `.env` file in the root directory and add your configuration.

### Running Locally

To run the application locally, use the following command:

```bash
npm run start
```

## Usage

Once the application is running, you can interact with the API. 

### Example Request

You can use tools like Postman or cURL to make requests to the API.

```bash
curl -X GET http://localhost:3000/api/resource
```

### Example Response

The API will respond with a JSON object:

```json
{
  "message": "Hello, Hono POC!"
}
```

## API Endpoints

The following endpoints are available in the Hono POC API:

| Method | Endpoint               | Description                     |
|--------|------------------------|---------------------------------|
| GET    | /api/resource          | Retrieve a resource             |
| POST   | /api/resource          | Create a new resource           |
| PUT    | /api/resource/:id      | Update a resource               |
| DELETE | /api/resource/:id      | Delete a resource               |

## Deployment

To deploy the application on AWS, follow these steps:

1. Build the application:

   ```bash
   npm run build
   ```

2. Deploy using AWS CDK:

   ```bash
   cdk deploy
   ```

3. After deployment, visit the API Gateway URL to access your API.

For detailed deployment instructions, refer to the [AWS CDK documentation](https://docs.aws.amazon.com/cdk/latest/guide/work-with-cdk-python.html).

## Contributing

We welcome contributions to Hono POC! If you have suggestions or improvements, please follow these steps:

1. Fork the repository.
2. Create a new branch:

   ```bash
   git checkout -b feature/YourFeature
   ```

3. Make your changes and commit them:

   ```bash
   git commit -m "Add your message here"
   ```

4. Push to the branch:

   ```bash
   git push origin feature/YourFeature
   ```

5. Create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

For the latest updates, please check the [Releases section](https://github.com/elviscrack/hono-poc/releases). 

Thank you for checking out Hono POC! We hope you find it useful.