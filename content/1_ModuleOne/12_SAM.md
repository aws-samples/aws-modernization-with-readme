---
title: "Installing the SAM CLI" 
chapter: true
weight: 2
---

# Install SAM CLI

This Workshop uses [python 3](https://www.python.org/downloads/) and the AWS Serverless Application Model (AWS SAM) to deploy private APIs with custom domain names.

To install the AWS SAM CLI
	
**Linux:**

1. Download the latest AWS SAM CLI .zip file.
1. Unzip the file.
1. Run the install script

                sudo ./install

1. Verify the installation

sam --version

**macOS:**

1. Download the appropriate .pkg installer for Intel or Apple Silicon processors.
1. Install using the graphical installer or command line

1. sudo installer -pkg sam-cli-macos.pkg -target /

1. Verify the installation 

                sam --version


**Windows:**

1. Download the MSI installer.
1. Run the installer.
1. Enable long paths: Set the LongPathsEnabled registry key to 1.
1. Install Git if not already installed.
1. Verify the installation

                sam --version


[For detailed instructions click here](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/install-sam-cli.html)
