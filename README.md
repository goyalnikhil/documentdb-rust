# How to Use Amazon DocumentDB with Rust - A Step-by-Step Guide
## Introduction

This sample project will create a Rust application that executes CRUD operations on an existing Amazon DocumentDB cluster. It will use AWS Secretes Manager to retrieve database credentials and connect to the Amazon DocumentDB cluster.

Project contains a <code>Cargo.toml</code> file with required dependencies and <code>main.rs</code> contains the main source code in Rust programming language.

## Prerequisites

You should have an existing Amazon DocumentDB cluster in your AWS account. Also needed is an EC2 instance that can connect to the DocumentDB cluster. Follow [Getting started with <link>Amazon DocumentDB (with MongoDB compatibility); Part 1 – using Amazon EC2](https://aws.amazon.com/blogs/database/part-1-getting-started-with-amazon-documentdb-using-amazon-ec2/) for detailed steps on creating a cluster and connecting to it from an Amazon EC2 instance.



Finally, you will need to store the database credentials in AWS Secretes Manager. For more information on how to create a secret refer to [AWS Secrets Manager user guide](https://docs.aws.amazon.com/secretsmanager/latest/userguide/create_secret.html). The secret name created in this step will be used later in the setup.

## Step 1: Setup on EC2 instance

The On the EC2 instance, Rust should be installed. Follow installation steps at [Install Rust](https://www.rust-lang.org/tools/install). Validate the Rust installation by running <code>rustc --version</code>.

Using below git command, clone repository in to the home directory of your EC2 instance.
```
git clone https://github.com/goyalnikhil/documentdb-rust.git
```
Also, download the AWS RDS global certificates bundle and save it your preferred location on your EC2 instance. Full path to this certificate will be needed later on.
```
wget https://truststore.pki.rds.amazonaws.com/global/global-bundle.pem
```

## Step 2: Update Rust source code

While in the <code>documentdb-rust</code> folder, open <code>src/main.rs</code> file in your choice of editor and make changes by replacing:
- <code>Your-Seceret-Name</code> with the name of secrete you created in AWS Secretes Manager with DocumentDB credentials.
- <code>Path-to-global-bundle</code> with the full path name of the location you stored the downloaded <code>global-bundle.pem</code> file.
Save the file and exit the editor. Your Rust code is ready to compile and run.

## Step 3: Build and run

We use Rust's inbuilt package manager <code>Cargo</code> for compiling, building, and running the application. While still in the <code>documentdb-rust</code> folder, run command listed below. <code>Cargo</code> will download the needed packages, compile them, and finally build a binary for the source code in the <code>src</code> folder. This could take a while.
```
cargo build
```

