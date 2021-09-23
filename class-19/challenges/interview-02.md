# Interview 02

Ask the candidate:
  - What is the difference between an IAM role and an IAM user?
  - What are the managed policies in AWS IAM?
  - Share this code snippet with the candidate. Ask: What is this piece of code and what does it do?
    ```
    {
      "Version":"2020-3-20",
      "Statement":[
        {
          "Effect":"Allow",
          "Action":[
            "s3:PutObject",
            "s3:GetObject",
            "s3"GetObjectVersion",
            "s3:DeleteObject",
            "s3:DeleteObjectVersion"
          ],
          "Resource":"arn:aws:s3:::example_bucket/example_folder/*"
        }
      ]
    }
    ```
  - What is a policy summary, and can you show me an example of one?

## Interviewer Notes

Key areas to explore and discuss:

- "The two key differences between the IAM role and IAM user are:
  - An **IAM role** is an IAM entity that defines a set of permissions for making AWS service requests, while an **IAM user** has permanent long-term credentials and is used to interact with the AWS services directly.  
  - In the IAM role, trusted entities, like IAM users, applications, or an AWS service, assume roles whereas the IAM user has full access to all the AWS IAM functionalities."  -[Simplilearn](https://www.simplilearn.com/tutorials/aws-tutorial/aws-interview-questions) 
- "There are two types of managed policies; one that is managed by you and one that is managed by AWS. They are IAM resources that express permissions using IAM policy language. You can create, edit, and manage them separately from the IAM users, groups, and roles to which they are attached." -[Simplilearn](https://www.simplilearn.com/tutorials/aws-tutorial/aws-interview-questions) 
- This is an IAM policy that grants permission to add, update, and delete objects from the folder `example_bucket/example_folder/*`.
- The AWS Console summarizes policies at a glance instead of having to review JSON tables.
