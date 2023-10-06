# Take-Home Assignment: Designing a Distributed Cache System for GitHub and GitLab Data

## Assignment Duration

Please note that this assignment is designed to be completed within 1 hour. We deeply value your time and commitment to this assessment.

## Reward

Upon successful completion of this assignment, you will receive a $100 gift card as a token of our appreciation for your efforts and time.

## Problem Description

You are tasked with designing a distributed cache system to improve the performance and reduce the impact on rate limiting when querying GitHub and GitLab data through a GraphQL backend of our platform. The goal is to efficiently store and retrieve data from GitHub and GitLab while ensuring data privacy, consistency, and synchronization across a distributed environment.

## Assignment

Your task is to whiteboard the design of a distributed cache system that can effectively store and manage GitHub and GitLab data.

Your team has a javascript UI that is making a call to an API which is then calling GitHub and GitLab, and the users are reporting rate limiting. The historical git data typically remains static and only the latest changes for a repo tend to be dynamic. The queries the team's API are using are already optimized.

With all this in mind, design a distributed cache system for the team that will significantly cut down on rate limiting.

## Submission

Your solution can be a whiteboard diagram or a written description of your cache system design, addressing all the key aspects mentioned above. If you use a whiteboard diagram, please provide annotations and explanations as needed.

## Evaluation Criteria

- Completeness and correctness of the cache system design.
- Consideration of cache technology, data structure, and eviction policies.
- Handling of distributed synchronization and data privacy.
- Strategies for ensuring data consistency and cache scalability.

**Note:** This assignment assesses your system design skills, particularly in the context of caching and distributed systems. The goal is to create a robust and efficient cache system that enhances the performance of the GraphQL backend while addressing important considerations like data privacy and consistency. Good luck with the assignment!