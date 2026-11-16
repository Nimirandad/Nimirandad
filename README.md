## Hi, I'm Nicolás Miranda

Backend engineer from Chile with 6 years of experience. I work at Sovos on the backend of an identity verification platform (face biometrics, document checks) used in Chile, Peru, Mexico and Argentina.

**What I've been working on lately**

A Go service that handles the lifecycle of customers' facial verification data:

- Exports a customer's transactions for a date range to CSV, copies the images to their storage (S3 or Azure Blob) and emails the result.
- Runs scheduled bulk image copies between S3 and Azure, per customer.
- Deletes all data for a customer across MySQL, S3 and DynamoDB, with a report per phase.
- Deletes one person's biometric data by document number (privacy requests). It builds a signed deletion plan first, then runs it asynchronously and coordinates with external systems.

Under the hood it has a task scheduler configured in the database, with priorities, distributed locking across replicas and automatic retry of failed date ranges. It runs on Kubernetes and has OpenTelemetry tracing, Prometheus metrics and logs that mask personal data.

**What I use day to day**

- Go and Node.js
- AWS (ECS, EKS, Lambda, S3, DynamoDB, SNS) and Azure Blob Storage
- MySQL and PostgreSQL
- Docker, Kubernetes, Terraform
- REST APIs with OpenAPI, CI/CD with Jenkins and Azure Pipelines

**Contact**

[LinkedIn](https://www.linkedin.com/in/nicolas-miranda-delgado-a2230a194)
