# GitHub Action: s3 sync

This GitHub Action automates the process of upload on s3 assets.

## Examples
```yaml
    -
      name: sync on s3
      uses: devredops/cicd-s3-sync@main
      with:
        aws-region: ${{ vars.AWS_REGION }}
        aws-role-to-assume: ${{ vars.AWS_ROLE_TO_ASSUME }}
        aws-s3-sync-extra-params: "--delete"
        source-full-path: "build"
        destination-bucket-name: ${{ vars.PACKAGE_S3_BUCKET_NAME }}
        destination-path: "/"
        aws-cloudfront-distribution-id: ${{ vars.DISTRIBUTION_ID }}
```

