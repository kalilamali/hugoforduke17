# hugoforduke17
This is a sample hugo website for a duke Class


This website was created using [Hugo] (https://gohugo.io/)

1. Create an AWS Cloud9 environment

2. Change the inbound rules in AWS Cloud9 to allow outside traffic
i![inbound_rules_aws](https://github.com/kalilamali/hugoforduke17/assets/47039819/1e040304-e4df-4774-a5fc-be292275bd46)
o/releases

3. Get Hugo and put the program in the path of AWS Cloud9
https://github.com/gohugoio/hug

4. Follow the hugo commands to create a new website

```bash
hugo new site quickstart
cd quickstart
git init
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
echo "theme = 'ananke'" >> hugo.toml
hugo server
```

3. Create an AWS S3 bucket

4. Check the static website hosting option

5. Download the contents of the public folder

6. Upload the contents of the public folder in Objects in the AWS S3 bucket

7. Turn off the option Block all public access in the AWS S3 bucket

8. Add a bucket policy:


{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::hugowebsiteduke/*"
        }
    ]
}

9. Find the link to the website in Properties in the AWS S3 bucket
![hugo_website](https://github.com/kalilamali/hugoforduke17/assets/47039819/e5676a94-0f48-4ded-b0a7-abc9a5b50304)

10. DONE! :)
