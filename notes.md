AWS:

performance gains bc of how the users get the code they interact with 

[]Hosted on AWS via S3
[]Distributed Globally
[]Secured with SSL
[]Automatically Deployed with CI/CD
[]Dynamically responding to requests

This information can be combined with the knowledge from the Lambda / Serverless Course! 


Root users have unrestricted access
IAM users will perform 'daily' tasks

Continuous Integration / Continuous Delivery

-Using IAM:
    - Create accounts that handle tasks so that the root user account isn't used (security)
    - Establish user groups so it streamlines access and permissions ... but you can also copy permissions from an existing user
    - AWS has built in policies that we can attach directly
    - Tags let you insert metadata so you cna quickly find product / team / etc 

