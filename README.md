## AWS Amplify Next.js (Pages) Starter Template

This repository provides a starter template for creating applications using Next.js (Pages) and AWS Amplify, emphasizing easy setup for authentication, API, and database capabilities.

## Overview

This template equips you with a foundational Next.js application integrated with AWS Amplify, streamlined for scalability and performance. It is ideal for developers looking to jumpstart their project with pre-configured AWS services like Cognito, AppSync, and DynamoDB.

## Setup
- Clone this repository from [AWS Documentation link](https://docs.amplify.aws/nextjs/start/quickstart/nextjs-pages-router/)
- Create `App` from AWS Amplify console, by selecting `Git Hub`
- Ensure the `Build` YAML is edited. Add these phases before `build` phase

```yaml
    preBuild:
      commands:
        - nvm use 20
```
- Wait for Build & Deployment process
  - **Result:** <span style='color:green'>OK</span>
 
- Follow the steps in [AWS Documentation link](https://docs.amplify.aws/nextjs/start/quickstart/nextjs-pages-router/)

### Sandbox

- Make sure to set Env Var before launching Sandbox (an Isolated environment for development)

```bash
export AWS_REGION=ap-southeast-1
npx ampx sandbox
```

>**Note:**
>- Creation of Sandbox results in launch of a separate CloudFormation stack
>- After successful launch of stack, you will find `amplify_outputs.json` updated with updated connection informaton referring to sandbox

- Sandbox environment runs as a `foreground` job
  - This is essentially the `local backend` 
- Once Sandbox environment is ready, open another Terminal and launch `frontend`
- Launch `http://localhost:3000` and re-register a `user email`
- You should see the updated Welcome page
  - **Result:** <span style='color:green'>OK</span>


## Features

- **Authentication**: Setup with Amazon Cognito for secure user authentication.
- **API**: Ready-to-use GraphQL endpoint with AWS AppSync.
- **Database**: Real-time database powered by Amazon DynamoDB.

## Deploying to AWS

For detailed instructions on deploying your application, refer to the [deployment section](https://docs.amplify.aws/nextjs/start/quickstart/nextjs-pages-router/#deploy-a-fullstack-app-to-aws) of our documentation.

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.