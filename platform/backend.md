# Take-Home Assignment: Designing a Unified GraphQL Schema for GitHub and GitLab Repositories

## Assignment Duration

Please note that this assignment is designed to be completed within 1 hour. We deeply value your time and commitment to this assessment.

## Reward

Upon successful completion of this assignment, you will receive a $100 gift card as a token of our appreciation for your efforts and time.

## Problem Description

You are tasked with designing a GraphQL schema that unifies Git repositories from both GitHub and GitLab. The schema should allow for querying repositories without distinguishing between GitHub and GitLab sources. Additionally, you need to conceptualize a GraphQL query for repositories and implement pagination.

## Assignment

Your task is to design the unified GraphQL schema, including the types, fields, and queries necessary for fetching repositories from GitHub and GitLab. To highlight the differences in the data structures between GitHub and GitLab, we'll provide you with schema samples for both platforms. Your goal is to reconcile these differences and create a unified schema.

1. **GitHub and GitLab Schema Samples** (Conceptualized):
   **GitHub Repository Schema Sample:**

   ```graphql
   type GitHubRepository {
     name: String!
     description: String
     refs: {
       name: string
       totalCount: Int!
     }
   }
   ```

   **GitLab Repository Schema Sample:**

   ```graphql
   type GitLabRepository {
     name: String!
     description: String
     branches: {
       id: string;
       totalCount: Int!
     }
   }
   ```

   Note the difference in field names: GitHub uses `refs`, while GitLab uses `branches`.

2. **Unified GraphQL Schema** (Your Task):
   - Conceptualize and define a unified GraphQL schema that combines GitHub and GitLab repositories into a single type.
   - Account for the differences in field names (`refs` vs. `branches`) between GitHub and GitLab.
   - Ensure that the unified schema includes fields such as `name`, `description`, and `branchCount`.

3. **GraphQL Query and Pagination** (Your Task):
   - Design a GraphQL query for fetching repositories from the unified schema.
   - Implement pagination to retrieve a specified number of repositories at a time.
   - Include arguments for filtering and sorting repositories (e.g., owner, language).
   - How would you scale pagination when searching for repos between two seperate graphs?

## Submission

You can submit your solution as a written GraphQL schema and query design. Include any additional notes or explanations that clarify your design choices, especially regarding how you handled the field name disparity between GitHub and GitLab.

## Evaluation Criteria

- Correctness and completeness of the unified GraphQL schema.
- Design of a GraphQL query for fetching repositories with pagination.
- Consideration of best practices in GraphQL schema design.
- Handling of field name disparities between GitHub and GitLab.

**Note:** This assignment highlights the challenge of unifying GraphQL schemas with different field names (e.g., `refs` vs. `branches`) and focuses on schema design and query conceptualization. You do not need to implement the entire solution, as the primary goal is schema design. Good luck with the assignment!