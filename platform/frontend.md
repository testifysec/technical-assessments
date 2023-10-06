# Take-Home Assignment: GitHub Repo List React App

## Assignment Duration

Please note that this assignment is designed to be completed within 1 hour. We deeply value your time and commitment to this assessment.

## Reward

Upon successful completion of this assignment, you will receive a $100 gift card as a token of our appreciation for your efforts and time.

## Conceptual App Description

Imagine you are building a React app that interacts with the GitHub GraphQL API. The app's primary purpose is to search for GitHub repositories and display them in a list format. You will be provided with a typescript type that represents the data returned by this graph. Your task is to use the TypeScript types to represent this data and then implement a React hook and component to display a list of repositories based on the GraphQL response.

**GraphQL Query Example:**
Below is the hypothetical GraphQL query example that you your app might have used to fetch repository data from GitHub:

```graphql
query SearchRepos($query: String!, $limit: Int!) {
  search(query: $query, type: REPOSITORY, first: $limit) {
    edges {
      node {
        ... on Repository {
          name
          description
          refs(refPrefix: "refs/heads/") {
            totalCount
          }
        }
      }
    }
  }
}
```

**TypeScript Types:**
To work with the GraphQL response, we have defined TypeScript types as follows:

```typescript
type SearchReposResponse = {
  data: {
    search: {
      edges: {
        node: {
          name: string;
          description: string | null;
          refs: {
            name: string;
            totalCount: number;
          };
        };
      }[];
    };
  };
};

type Repo = {
  name: string;
  description: string | null;
  branchCount: number;
};
```

**Explanation of TypeScript Types:**

- `SearchReposResponse` corresponds to the overall response structure from the GraphQL query. It contains a `data` field that has a `search` field, which has an array of `edges`. Each `edge` contains a `node` with the repository details.

- `Repo` is a simplified type that matches the structure of the repository data you want to map. It includes `name`, `description`, and `branchCount` based on the GraphQL query.

## Assignment

1. Create a React hook named `useGitHubRepos` that returns a `SearchReposResponse` (hardcoded is fine). You can use mock data to simulate the GraphQL response. The hook should have the following structure:

```typescript
import { SearchReposResponse } from './types';

function useGitHubRepos(query: string, limit: number): SearchReposResponse {
  // Implement the hook logic here and return a hardcoded response.
}

export default useGitHubRepos;
```

2. Create a React component named `RepoList` that uses the `useGitHubRepos` hook to fetch and display a list of GitHub repositories based on the GraphQL response. The component should render the repository name, description, and the number of branches for each repository.

3. You can style the `RepoList` component as you see fit, but focus on functionality over extensive styling within the given time frame. Responsive design is encouraged, and you can use any npm packages you like.

4. Ensure the component is responsive and user-friendly.

## Submission

You can submit your solution in a code snippet, a CodeSandbox, a GitHub Gist, or any other format that you prefer.
We'll talk over your approach and ask questions.

## Evaluation Criteria

- Functionality: Does the `RepoList` component correctly fetch and display GitHub repositories using the `useGitHubRepos` hook?
- Code Quality: Is the code well-organized, clean, and easy to understand?
- UI/UX: Is the user interface clean and user-friendly?
- TypeScript Types: Are the provided TypeScript types correctly used in your code?
- Responsiveness: Is the component responsive on different screen sizes?

**Note:** You have a maximum of 1 hour to complete this assignment. Focus on the core functionality and simple patterns. This is so we can understand how your approach problems and talk abotu them. We do not wish to take much  of your time. Good luck with the assignment!