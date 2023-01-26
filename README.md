Developer creates claim for XServerlessApp:

# XServerlessApp
API: ./demo-app/manifests/composition/definition.yaml
Composition: ./demo-app/manifests/composition/object-processor.yaml

API for developers:
 - bucketName: crossplane-serverless
 - bucketKey: function.zip
(TODO document other params)

Resources:
* XFanout
  API: ./demo-infra/compositions/sns-sqs/definition.yaml
  Composition: ./demo-infra/compositions/sns-sqs/sns-sqs.yaml

* EventSourceMapping
  API: ./demo-infra/compositions/event-source-mapping/definition.yaml
  Composition: ./demo-infra/compositions/event-source-mapping/sqs.yaml

* XLambdaFunction
  API: ./demo-infra/compositions/lambda/definitions.yaml
  Composition: ./demo-infra/compositions/lambda/zip.yaml

* XObjectStorage
  API: ./demo-infra/compositions/s3/definition.yaml
  Composition: ./demo-infra/compositions/s3/general-purpose.yaml

* IAMPolicies
  API: ./demo-infra/compositions/iam-policy/definition.yaml
  Compositions: ./demo-infra/compositions/iam-policy