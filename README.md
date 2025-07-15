# Mintlify Starter Kit

Click on `Use this template` to copy the Mintlify starter kit. The starter kit contains examples including

- Guide pages
- Navigation
- Customizations
- API Reference pages
- Use of popular components

### Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) to preview the documentation changes locally. To install, use the following command

```
npm i -g mint
```

Run the following command at the root of your documentation (where docs.json is)

```
mint dev
```

### Publishing Changes

Install our Github App to auto propagate changes from your repo to your deployment. Changes will be deployed to production automatically after pushing to the default branch. Find the link to install on your dashboard. 

#### Troubleshooting

- If the dev environment isn't running - Run `mint update` to ensure you have the most recent version of the CLI.
- Page loads as a 404 - Make sure you are running in a folder with `docs.json`

---

## Understanding the `.deploxy.json` file

This file holds the configuration for your Deploxy deployment. Here's a breakdown of its properties:

-   `authToken`: This is the token required to authenticate and deploy your package to Deploxy.

-   `defaultDeployRegion`: This is the default AWS region where your MCP server will run if the end-user does not specify a particular region. When you deploy a package with Deploxy, your MCP server logic is deployed to serverless environments in regions all over the world. To give your end-users the fastest experience, they can specify a region using the `--region` flag when they run your package:
    ```bash
    npx -y your-pkg --region us-east-1
    ```
    If the `--region` parameter is omitted, the `defaultDeployRegion` you set in this file will be used to handle the user's request.
    > With the Deploxy Pro plan, the `--region` parameter is not needed. Requests are automatically routed to the nearest region for the end-user.

-   `stdioArgsIndex`: This option specifies the arguments that are passed directly to your MCP server. For example, when an end-user runs the following command:
    ```bash
    npx -y your-pkg --args user-api-key user-token
    ```
    Your server can access `user-api-key` and `user-token` from `process.argv`.

-   `injectedEnv`: This is an object of environment variables that are accessible only within your MCP server. You can access them in your code using `process.env.DATABASE_URL`, for example.
    
    Wondering how end-users can't see these? Don't worry. The end-user never sees or has access to your actual MCP server code.
    
    To understand how this works, you need to follow this Quick Start and deploy your package. In short, the code that the end-user downloads and runs via `npx` is a lightweight **proxy client**. This proxy client takes user requests (like a ToolCall) and streams them to your actual MCP server, which is running securely in the serverless cloud. This architecture allows you to focus on your core business logic without worrying about exposing sensitive information. You'll understand immediately once you inspect your published package on NPM after deployment.

-   `mcpPath` and `packageType`: You generally don't need to change these.