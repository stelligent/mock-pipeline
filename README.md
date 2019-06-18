# mock-pipeline

Use Mock Pipeline to model [value stream maps](https://en.wikipedia.org/wiki/Value-stream_mapping) regardless of your tech stack, cloud provider, or data center. With Mock Pipeline, you can define your value stream map as code in order to visualize all the steps in your commit to production lifecycle. While it uses AWS services/tools such as [AWS CloudFormation](https://aws.amazon.com/cloudformation/) and [AWS CodePipeline](https://aws.amazon.com/codepipeline/), it can model _any_ technology platform. 

For a description of the purpose of Mock Pipeline, see [Technological Accelerants for Organizational Transformation](https://www.youtube.com/watch?v=42gDK3MDuJI&feature=youtu.be&t=1647) and see [Value Stream Mapping with Mock Pipeline](https://stelligent.com/2019/04/15/value-stream-mapping-with-mock-pipeline/) for a detailed description on how to use Mock Pipeline.

## Setup
These instructions assume you're using [AWS Cloud9](https://aws.amazon.com/cloud9/). Adapt the instructions if you're using a different IDE.

[Fork](https://help.github.com/en/articles/fork-a-repo) this repo: https://github.com/stelligent/mock-pipeline

From Cloud 9, clone the newly forked repo (replacing `USERNAME` in the example).

```
git clone https://github.com/USERNAME/mock-pipeline.git
cd mock-pipeline
sudo su
sudo curl -s https://getmu.io/install.sh | sh
exit
```

Make any modificiations to your _local_ [mu.yml](./mu.yml#LL47) file (in your Cloud9 IDE in this example) for the stages and actions you want to model. Commit them to your repo.

```
git commit -am "modify stages and actions" && git push
```

To create this pipeline in your account, run: `mu pipeline up -t GITHUBTOKEN`

Your `GITHUBTOKEN` will look something like this: `2bdg4jdreaacc7gh7809543d4hg90EXAMPLE`. To get or generate a token, go to [GitHub's Token Settings](https://github.com/settings/tokens).

After a few of the CloudFormation stacks have launched, go to the [CodePipeline console](https://console.aws.amazon.com/codesuite/codepipeline/pipelines/) and look for a pipeline with something like `mock-pipeline` in its name. Select this pipeline and ensure you are properly connected to the GitHub repository you'd previously forked. 


## Additional Resources
See [Value Stream Mapping with Mock Pipeline](https://stelligent.com/2019/04/15/value-stream-mapping-with-mock-pipeline/) for a detailed description on how to use Mock Pipeline.


See [Metric Details](https://github.com/stelligent/pipeline-dashboard#metric-details) for more information on release metrics such as Cycle Time, Lead Time, and MTTR. 
