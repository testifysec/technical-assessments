# Take-Home Assignment: Designing a Continuous Delivery Pipeline for a React and Go Application on Kubernetes

## Assignment Duration

Please note that this assignment is designed to be completed within 1 hour. We deeply value your time and commitment to this assessment.

## Reward

Upon successful completion of this assignment, you will receive a $100 gift card as a token of our appreciation for your efforts and time.

## Problem Description

Imagine you are tasked with designing a continuous delivery pipeline for a web application. The application consists of a React frontend and a Go backend, and it needs to be deployed continuously to a Kubernetes cluster. Your goal is to outline the key components and steps involved in setting up an efficient and reliable continuous delivery process.

## Assignment

Your task is to create a high-level whiteboard diagram or a written outline that describes the components and steps involved in building a trunk-based, continuous delivery pipeline for this application. Here are the main points to cover:

1. **Trunk-based Dev and Continuous Delivery**:
   - In Contiuous Delivery with Trunk-Based dev, The `main` branch is trunk, and production must always continuously have latest from `main`. Devs will branch off trunk to iterate in `shortlived-environments` before merging to trunk. How can your pipeline support this kind of strategy?

2. **Continuous Integration**:
   - Describe the process of getting source, building, linting, and testing both the React frontend and Go backend.
   - How will these stages be executed? Are you using shell commands? (Consider that our open source tool [witness](www.github.com/testifysec/witness) observes shell commands and records evidence trails, could you use witness to secure this pipeline?)
   - Discuss security measures for your pipeline, including image scanning, vulnerability checks, and access control.
   - Specify the build tools, scripts, or CI/CD platforms you plan to use.
   - Specify the triggers and conditions for automatic deployments.
   - Discuss rollback and incident response strategies.

3. **Continuous Deployment to Kubernetes**:
   - Detail how your Kubernetes cluster will be set up.
   - Explain how the React and Go applications will be deployed and scaled.

## Submission

You can submit your solution as a written outline or a high-level whiteboard diagram. Feel free to use any drawing or diagramming tools if you choose the whiteboard approach.

## Evaluation Criteria

- Clarity and completeness of the design for the continuous delivery pipeline.
- Consideration of best practices for DevOps and Kubernetes.
- Understanding of key components and their interactions.
- Alignment with modern CI/CD and containerization principles.

**Note:** This assignment is intended to assess your DevOps and infrastructure design skills. It's important to think through the process thoroughly, but you do not need to implement the pipeline itself. Good luck with the assignment!