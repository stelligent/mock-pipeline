# mock-pipeline

Use Mock Pipeline to model [value stream maps](https://en.wikipedia.org/wiki/Value-stream_mapping) regardless of your tech stack, cloud provider, or data center. With Mock Pipeline, you can define your value stream map as code in order to visualize all the steps in your commit to production lifecycle. While it uses AWS services/tools such as [AWS CloudFormation](https://aws.amazon.com/cloudformation/) and [AWS CodePipeline](https://aws.amazon.com/codepipeline/), it can model _any_ technology platform. 

To see a video describing Mock Pipeline, see [Technological Accelerants for Organizational Transformation](https://www.youtube.com/watch?v=42gDK3MDuJI&feature=youtu.be&t=1647).

## Setup
These instructions assume you're using [AWS Cloud9](https://aws.amazon.com/cloud9/). Adapt the instructions if you're using a different IDE. 

```
sudo su
sudo curl -s https://getmu.io/install.sh | sh
```

To create this pipeline in your account, run: `mu pipeline up`

See [Metric Details](https://github.com/stelligent/pipeline-dashboard#metric-details) for more information on release metrics such as Cycle Time, Lead Time, and MTTR. 
