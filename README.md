# aws-deploy-pipeline

CI/CD pipelines using GitHub Actions to deploy to AWS — static sites to S3
and container images to ECR.

## What it does

**S3 workflow** (`deploy.yml`)
- Triggers on push to main
- Builds and syncs a static site to an S3 bucket
- Currently deploys my portfolio site

**ECR workflow** (`deploy-ecr.yml`)
- Manually triggered (workflow_dispatch)
- Checks out an external application repo, builds its Docker image, and
  pushes it to Amazon ECR
- Currently builds [Spectra Stream](https://github.com/dtorres47/spectra-stream),
  a Ko-fi quest storefront and live stream overlay (C#/.NET), which runs on
  AWS ECS (Fargate + ALB via Express Mode)
- Designed to work with any source repo containing a Dockerfile at its root

## Future enhancements

- Add testing and linting steps to the workflows
- Integrate additional portfolio projects