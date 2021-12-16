# FusionAuth Webhooks

This example uses lambda to handle a Fusionauth webhook.

## Prerequisites

* AWS account
* CDK installed: https://docs.aws.amazon.com/cdk/latest/guide/getting_started.html
* FusionAuth installed: https://fusionauth.io/docs/v1/tech/installation-guide/

## Building

To build this app, run `mvn compile`. This will download the required
dependencies to compile the Java code.

You can use your IDE to write code and unit tests, but you will need to use the
CDK toolkit if you wish to synthesize/deploy stacks.

## CDK Toolkit

The [`cdk.json`](./cdk.json) file in the root of this repository includes
instructions for the CDK toolkit on how to execute this program.

Specifically, it will tell the toolkit to use the `mvn exec:java` command as the
entry point of your application. After changing your Java code, you will be able
to run the CDK toolkit commands as usual (Maven will recompile as needed):

    $ cdk ls
    <list all stacks in this program>

    $ cdk synth
    <cloudformation template>

    $ cdk deploy
    <deploy stack to your account>

    $ cdk diff
    <diff against deployed stack>

Based off of the AWS CDK examples: https://github.com/aws-samples/aws-cdk-examples

## Integration

* Add a webhook endpoint in FusionAuth: https://fusionauth.io/docs/v1/tech/events-webhooks/
* Take actions and see the events show up in s3.

## Todo

* Implement an API key so that not everyone can send info to this webhook.
* Blog post.
