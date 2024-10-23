# How to Use Amazon DocumentDB with Rust - A Step-by-Step Guide
## Introduction

This sample project will create a Rust application that executes CRUD operations on an existing Amazon DocumentDB cluster. It will use AWS Secretes Manager to retrieve database credentials and connect to the Amazon DocumentDB cluster.

Project contains a <code>Cargo.toml</code> file with required dependencies and <code>main.rs</code> contains the main source code in Rust programming language.

## Prerequisites

You should have an existing Amazon DocumentDB cluster in your AWS account. Also needed is an EC2 instance that can connect to the DocumentDB cluster. Follow [Getting started with <link>Amazon DocumentDB (with MongoDB compatibility); Part 1 – using Amazon EC2](https://aws.amazon.com/blogs/database/part-1-getting-started-with-amazon-documentdb-using-amazon-ec2/) for detailed steps on creating a cluster and connecting to it from an Amazon EC2 instance.

On the EC2 instance, Rust should be installed. Follow installation steps at [](

Finally, you will need to store the database credentials in AWS Secretes Manager. For more information on how to create a secret refer to [AWS Secrets Manager user guide](https://docs.aws.amazon.com/secretsmanager/latest/userguide/create_secret.html)

