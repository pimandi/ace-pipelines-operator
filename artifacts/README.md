# Deployment order:

#### Create pipeline resources in this order

1. PipelineResource: GIT (Note: update the Repo URL as needed)
2. PipelineResource: Image
3. PipelineTask: DockerF Build Push
4. PipelineTask: Deploy ACE Img
5. Pipeline: ACE CICD (Note: adjust the default namespace to match your own environment)
6. PipelineTriggerTemplate: ACE CICD
7. PipelineEventListener: ACE CICD
8. PipelineRoute: Event Listener ACE CICD
