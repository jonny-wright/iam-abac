# iam-abac

* How frequently can we call STS assume role (the role session will likely only be used for a single operation before being discarded) 

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

## Sequence Diagram
![Sequence Diagram](ABAC.png)