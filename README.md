# s3-deploy-pipeline

A CI/CD pipeline using GitHub Actions to automatically deploy static sites to AWS S3.

## What it does

- Triggers deployment on push to main
- Syncs files to S3 bucket
- Currently deploys [Spectra Stream](https://github.com/dtorres47/spectra-stream), an interactive streaming overlay system

## Future enhancements

- Add testing and linting steps to the workflow
- Integrate additional portfolio projects
