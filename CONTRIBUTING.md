# Contributing

## `npm install`

In addition to installing dependencies, the project has been configured to run `npm audit fix` to resolve all non-breaking security vulnerabilities.

If you delete your package-lock.json you will receive an error.

In this case, you shall need to run `npm i -package-lock-only` first, before `npm install`

## Development

To run the unit tests: `npm test`

To deploy the CodeBuild project for staging the templates: `npm run create-codebuild` or `npm run update-codebuild`

To deploy to your account: `npm run deploy`
You can change the bucket via `npm config set pipeline-dashboard:staging_bucket my-bucket-name`


# Release

To Release:

1. Push your changes.
1. Bump the version in the `package.json`
2. Run the codebuild project in ap-southeast-2 to build the package + deploy the SAR

# TODO

* Review `pipline.yml` and deploy?

