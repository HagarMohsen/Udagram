
## Pipeline Infrastructure
**pipeline overview**
Whenever the developer pushes any code update the pipeline will be triggered.
1. CircleCi is triggered to start the build.
1. Checkout the code from the repository.
1. Install AWS & Elastic Beanstalk CLI.
1. Configure AWS Credentials.
1. Install frontend dependencies.
1. Install backend dependencies.
1. Build frontend.
1. Build backend.
1. Deploy frontend to S3.
1. Deploy backend to Elastic Beanstalk.
1. sit the eb environment variables.

![Pipeline Infrastructure](https://user-images.githubusercontent.com/74413831/153284808-87056606-3f46-4be4-96da-3f87bf75dae1.png)

**Last success circleci build**

![Pipeline Infrastructure](https://user-images.githubusercontent.com/74413831/153218446-ee1ec08f-d470-4837-9bd0-6fd364fd90ad.png)

**circleci Environment Variables**

![Pipeline Infrastructure](https://user-images.githubusercontent.com/74413831/153218512-54abfa3b-5f35-41ee-9215-3597b2cd8eed.png)


