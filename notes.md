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

- S3: [GLOBAL]
    - Simple Storage Service 
        - Take anything and store it on the cloud
        - In your account you have 'buckets'
            - You can put objects (files) in your buckets
            - You can read from your buckets
            - You can host web pages out of your buckets
        - Infinitely scalable / High Availability / High Durability 
        - Versioning
        - Encryption
        - Security
        - Uploading is free but you get charged for storage
        - You get charged for requests but can mitigate this
        - Bucket Names should be UNIQUE
        - Setup:
            - Disable ACL's
            - Block public buckets (disabled temporarily and add policies)


- Route 53 (for domains):
    - AWS's DNS
    - Makes hooking up a new domain really simple 
    - Pick a Domain! (.click is cheap)
        - Create a bucket and name it with the domain (us east 1?)
    


-- S3 & Policies:
    - What would you want a bucket for a public website to do?
        - Read access - no write access - no delete access
    - Permissions: 
        - Can be written as JSON
        - Can be generated using a generator on AWS
            - S3 Bucket Policy
            - Principal: *
            - Actions: 'GetObject' 
            - ARN: (bucket it can do the thing in
            - Example in REPO w/ Boilerplate

-- Adding things to the bucket!


AWS Command Line (checking and deploying):

```aws s3 ls://{bucketname}```

``` aws s3 cp build s3://{bucketname}```



