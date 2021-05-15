# Full stack React application using AWS Amplify

Getting started with AWS Amplify following this [tutorial](https://aws.amazon.com/getting-started/hands-on/build-react-app-amplify-graphql/).

- [Amplify CLI](#amplify-cli)
  - [Installation](#installation)
  - [Using Amplify CLI](#using-amplify-cli)
  - [Deleting resources](#deleting-resources)
- [Status](#status)

## Amplify CLI

### Installation

`npm install -g @aws-amplify/cli`

### Using Amplify CLI

- configuration:
  `amplify configure`

  Walkthrough [here](https://www.youtube.com/watch?v=fWbM5DLh25U).

  Initialization needs to be added for the application and for local use run `amplify pull --appId xxxxxxx --envName xxxxx`.

- authentication:

  - installation: `npm install aws-amplify @aws-amplify/ui-react`
  - create the authentication service: `amplify add auth`
  - deploy: `amplify push --y`
  - update the React project and set the CI/CD of the frontend and backend
  - trigger a new build

- API and db:

  - create the GraphQL API and db: `amplify add api`
  - update the schema as needed
  - deploy
  - view the GraphQL API in the account at any time: `amplify console api`
  - update the React project

- storage:

  - create the storage service: `amplify add storage`
  - update the GraphQL schema as needed
  - deploy
  - update the React project

### Deleting resources

- remove individual services:

  ```
  amplify remove auth
  amplify remove api
  amplify remove storage
  ```

- push the changes with `amplify push`
- delete the entire project and associated resources:
  `amplify delete`

## Status

**[COMPLETED]** - As I finished this tutorial, I am setting a personal status of "Completed" and will probably not update this repository in the near future as this was a learning project.
