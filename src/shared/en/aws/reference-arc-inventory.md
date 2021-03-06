# `npm run inventory`

> ✨ Take full control of the inventory of AWS resources generated by `npm run create`

Running `npm run inventory` displays an inventory of AWS resources represented by the current `.arc` file.

## Verify AWS Resources

Running `npm run inventory verify` verifies AWS resources for the current `.arc` file exist.

## Delete Everything Except DynamoDB Tables

Running `npm run inventory nuke` deletes all AWS resources for the current `.arc` file except for **DynamoDB tables**. DynamoDB tables can be deleted with an additional environment variable (explained below). This workflow makes it very fast to setup and teardown a single codebase across many infra deployments.

## Delete DynamoDB Tables

Running `ARC_NUKE=tables npm run inventory nuke` deletes all DynamoDB tables for the current `.arc` file.
