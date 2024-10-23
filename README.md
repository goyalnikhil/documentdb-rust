# How to Use Amazon DocumentDB with Rust - A Step-by-Step Guide
## Introduction

This sample project will create a Rust application that executes CRUD operations on an existing Amazon DocumentDB cluster. It will use AWS Secretes Manager to retrieve database credentials and connect to the Amazon DocumentDB cluster.

Project contains a Cargo.toml file with required dependencies and a main.rs source code.

## Prerequisets

You should have an existing Amazon DocumentDB cluster in your AWS account. Also needed is an EC2 instance that can connect to the DocumentDB cluster. Visit <> for a step-by-step guide on creating a cluster and connecting to the cluster from an EC2 instance.
Finally, you will need to store the database credentials in AWS Secretes Manager. Visit <> for more details.

