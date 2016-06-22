# Compile Functions

This plugins compiles the functions in `serverless.yaml` to CloudFormation resources.

## How it works

`Compile Functions` hooks into the [`deploy:compileFunctions`](/lib/plugins/deploy).

It loops over all functions which are defined in `serverless.yaml`.

Inside the function loop it creates corresponding lambda function resources which will be merged into the
`serverless.service.resources.Resources` section.