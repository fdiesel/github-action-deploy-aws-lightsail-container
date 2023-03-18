# github-action-deploy-aws-lightsail-container
Deploy container to AWS Lightsail

```yml
  steps:

    - name: Checkout repository
      uses: actions/checkout@v3

    - name: Build
      uses: docker/build-push-action@v4.0.0
      with:
        context: .
        push: false
        tags: registry/name:tag

    - uses: fdiesel/github-action-deploy-aws-lightsail-container@version
      with:
        image-name: name
        image: registry/name:tag
        aws-region: ${{ secrets.AWS_REGION }}
        aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
        aws-access-key: ${{ secrets.AWS_ACCESS_KEY }}
        aws-lightsail-service: ${{ secrets.AWS_LIGHTSAIL_SERVICE }}
        aws-lightsail-service-config: ${{ secrets.AWS_LIGHTSAIL_SERVICE_CONFIG }}
```
