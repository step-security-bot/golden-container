# golden-container
Trivial definition of an image build in compliance with Enterprise Contract policy

The latest built image is available at `quay.io/redhat-appstudio/ec-golden-image:latest`.

The image is signed and attested by Tekton Chains. For verification, use the
[staging public key](https://raw.githubusercontent.com/redhat-appstudio/infra-deployments/main/components/pipeline-service/public/tekton-chains-signing-secret.pub).

# To build in AppStudio

Best use `hack/rebuild.sh` from [ec-cli](https://github.com/enterprise-contract/ec-cli). To build manually create a `PipelineRun` based on [pull-request.yaml](./.tekton/pull-request.yaml).
Replace values wrapped in double curly brances, e.g. `{{ revision }}`, with the expected literal, e.g. `main`.
