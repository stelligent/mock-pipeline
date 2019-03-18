# mock-pipeline

You can use Mock Pipeline to model your value stream map regardless of your tech stack, cloud provider, or data center. With Mock Pipeline, you can define your value stream map as code to visualize all the steps in your commit to production lifecycle. While it uses AWS services/tools such as [AWS CloudFormation](https://aws.amazon.com/cloudformation/) and [AWS CodePipeline](https://aws.amazon.com/codepipeline/), you can use it with any technology platform you're using. 

## Cloud9

```
sudo su
sudo curl -s https://getmu.io/install.sh | sh
```

This repo creates a mock pipeline with [mu](https://getmu.io) similar to the Stelligent blog post [Mocking AWS CodePipeline pipelines with Lambda](https://stelligent.com/2016/02/15/mocking-aws-codepipeline-pipelines-with-lambda/).

To create this pipeline in your account, run: `mu pipeline up`

See [Metric Details](https://github.com/stelligent/pipeline-dashboard#metric-details) for more information on release metrics such as Cycle Time, Lead Time, and MTTR. 
