# hugoforduke17
This is a sample hugo website for a duke Class


This website was created using [Hugo] (https://gohugo.io/)

1. To start get Hugo and put the program in the path of AWS Cloud9
https://github.com/gohugoio/hugo/releases

2. Follow the hugo commands to create a new website

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

