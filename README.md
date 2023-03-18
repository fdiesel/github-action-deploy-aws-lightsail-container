# github-action-deploy-aws-lightsail-container
Deploy container to AWS Lightsail

```yml
  steps:

    ...

    - uses: fdiesel/github-action-deploy-aws-lightsail-container@version
      with:
        image-name: name
        image: fqn
        aws-region: ${{ secrets.AWS_REGION }}
        aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
        aws-access-key: ${{ secrets.AWS_ACCESS_KEY }}
        aws-lightsail-service: ${{ secrets.AWS_LIGHTSAIL_SERVICE }}
        aws-lightsail-service-config: ${{ secrets.AWS_LIGHTSAIL_SERVICE_CONFIG }}
```
