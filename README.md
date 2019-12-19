# iam-abac


## Policy
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:Get*",
                "s3:List*"
            ],
            "Resource": [
                "arn:aws:s3:::jmw-workflow",
                "arn:aws:s3:::jmw-workflow/projects/${aws:PrincipalTag/project}/*"
            ]
        }
    ]
}
```