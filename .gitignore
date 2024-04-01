# Terraform Pipeline Infrastructure Deployment

This CloudFormation template is designed to deploy the infrastructure required to support a Terraform pipeline. The pipeline includes the setup for storing Terraform state, locking the state file using DynamoDB, a CodeCommit repository to store Terraform code, and CodeBuild projects for planning and applying the Terraform code.

## Parameters

- **TerraformStateBucketName**: The name for the S3 bucket to store the Terraform state file.
- **TerraformStateLockTableName**: The name for the DynamoDB table used for locking the Terraform state file.
- **TerraformCodeCommitName**: The name for the CodeCommit repository to store Terraform code.
- **TerraformCodeBuildImage**: The Docker image used for the CodeBuild projects.

## Resources

### IAM Role

- **CodeBuildRole**: IAM role for the CodeBuild projects to plan and apply Terraform code.

### S3 Bucket

- **TerraformStateBucket**: S3 bucket to store the Terraform state file.
- **TerraformPipelineArtifactBucket**: S3 bucket to store pipeline artifacts.

### DynamoDB Table

- **TerraformStateLockTable**: DynamoDB table for locking the Terraform state file.

### CodeCommit Repository

- **TerraformCodeCommit**: CodeCommit repository to store Terraform code.

### CodeBuild Projects

- **TerraformCodeBuildPlan**: CodeBuild project to plan the Terraform code.
- **TerraformCodeBuildApply**: CodeBuild project to apply the Terraform code.

### CodePipeline

- **TerraformPipeline**: CodePipeline to automate the Terraform workflow.

## Usage

1. Deploy this CloudFormation template in your AWS account.
2. Provide values for the required parameters.
3. Once deployed, you can start using the Terraform pipeline by pushing Terraform code to the CodeCommit repository.
4. The pipeline will automatically trigger, plan, and apply changes to your infrastructure based on the Terraform code.

## Notes

- Make sure to review and customize the IAM policies attached to roles and permissions granted to CodeBuild and CodePipeline as per your security requirements.
- Adjust the CodeBuild build specifications (`BuildSpec`) to meet your specific Terraform workflow needs.

For any issues or questions, please refer to the documentation or contact the infrastructure team.

---

**Creator:** [Avinash Kumar](https://avinashvidyarthi.github.io)
