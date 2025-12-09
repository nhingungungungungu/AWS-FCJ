---
title: "AWS Developer Tools – Deploying .NET Apps on ARM-based Compute Platforms"
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---

# AWS Developer Tools – Deploying .NET Applications on ARM-based Compute Platforms

Author: Philippe El Asmar – May 08, 2025  
Category: .NET, Announcements, AWS .NET Development, AWS SDK for .NET, AWS Toolkit for Visual Studio, Developer Tools, Visual Studio

We are excited to announce that **AWS Deploy Tool for .NET** now supports deploying .NET applications to **ARM-based compute platforms** on AWS! Whether deploying from Visual Studio or using the .NET CLI, you can now target cost-efficient ARM infrastructures like AWS Graviton with the same smooth, familiar experience.

---

## Why Deploy to ARM?

ARM-based instances, such as **AWS Graviton**, offer excellent price/performance and energy efficiency—making them a smart choice for many .NET workloads. With this update, you can leverage the full power of ARM on supported services without changing your deployment workflow.

If you are already using AWS Deploy Tool for .NET, deploying to ARM is as simple as selecting an ARM-based compute option, such as **AWS Elastic Beanstalk** or **Amazon ECS with AWS Fargate**.

---

## Getting Started with Visual Studio

To start in Visual Studio:

1. Install the latest version of **AWS Toolkit for Visual Studio** from Visual Studio Marketplace (also called **AWS Toolkit with Amazon Q**).  
2. After installing the toolkit and configuring AWS credentials, right-click your project in Solution Explorer and select **Publish to AWS…**.  

You can choose from the following **Publish Targets** updated to support ARM-based architecture:

- ASP.NET Core App to AWS Elastic Beanstalk on Linux  
- ASP.NET Core App to Amazon ECS using AWS Fargate  
- Scheduled Task on Amazon ECS using AWS Fargate  
- Service on Amazon ECS using AWS Fargate  

In the **Target Configuration** pane, select **Edit settings**. On the settings screen, select **Project Build** on the left, then change **Environment Architecture** to **Arm64**. Finally, click **Publish** to deploy your application to the ARM platform.

---

## Getting Started with .NET CLI

To start from the .NET CLI:

1. Install the AWS Deploy Tool CLI via NuGet:

dotnet tool install --global Aws.Deploy.Tools

2. Start the deployment process:

dotnet aws deploy

The CLI will guide you to select a **Deployment Option**. Choose an option that supports ARM-based deployment and update **Environment Architecture** to **Arm64**, then press Enter to start deployment.

---

## Conclusion

With ARM-based compute options now supported in AWS Deploy Tool for .NET, deploying .NET applications to Graviton infrastructure is easier than ever. Enjoy better performance and cost efficiency without changing your existing workflow.

### Next Steps

- Try deploying your .NET application to ARM-based compute by installing or updating to the latest AWS Deploy Tool for .NET version.  
- Explore the **Developer Guide** and our **GitHub repo** for documentation and sample projects.  
- Feel free to create issues or pull requests with improvement ideas.

**Tags:** .NET, deploy, deployment, dotnet
