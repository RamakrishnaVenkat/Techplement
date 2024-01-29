# Techplement
# Static Counter Website on AWS

This repository provides a simple static website with a counter feature, ready to be hosted on AWS. The counter is incremented each time the website is visited.

## Prerequisites

Before deploying the website on AWS, make sure you have the following:

1. [AWS Account]
2. [AWS CLI]

Deployment Steps

1. Clone the Repository:**

    ```bash
    git clone https://github.com/your-username/static-counter-website.git
    cd static-counter-website
    ```

2. Update Counter Logic (Optional):**

    If you want to customize the counter logic, navigate to the `index.html` file and make adjustments as needed.

3. Create an S3 Bucket:**

    ```bash
    aws s3api create-bucket --bucket techplemet --region YOUR_REGION
    ```

4. Configure Bucket for Static Website Hosting:**

    ```bash
    aws s3 website s3://techplemet/ --index-document index.html
    ```

5. Upload Website Files to S3 Bucket:**

    ```bash
    aws s3 sync . s3://techplemet/
    ```

6. Access the Static Counter Website:**

    Your static counter website is now hosted on AWS S3. Access it using the endpoint:

    ```
    http://techplemet.s3-website-Asia Pacific (Mumbai) ap-south-1.amazonaws.com
    ```

Cleanup (Optional)

If you want to remove the resources created:

1. Delete S3 Bucket:**

    ```bash
    aws s3 rb s3://techplemet --force
    ```

2. Remove Local Clone (Optional):

    ```bash
    cd ..
    rm -rf static-counter-website
    ```
Have attached the images for your reference:
![image](https://github.com/RamakrishnaVenkat/Techplement/assets/91265544/b8fdcc61-8a90-469a-b4d7-b232d6956a54)(before login)
![image](https://github.com/RamakrishnaVenkat/Techplement/assets/91265544/beae0a67-275d-490e-8026-714058f49d2b)(login page)
![image](https://github.com/RamakrishnaVenkat/Techplement/assets/91265544/494e8058-e8e9-48df-840d-baec4f3a6222)(the dashboard)
![image](https://github.com/RamakrishnaVenkat/Techplement/assets/91265544/15071362-5183-4dd8-a5db-ca186bef0ca2)(the s3 service page to host the static website)
![image](https://github.com/RamakrishnaVenkat/Techplement/assets/91265544/bbaae093-a0ef-4a46-bef6-fb7c54438061)(the new bucket has been highlighted)
![image](https://github.com/RamakrishnaVenkat/Techplement/assets/91265544/ac2910f9-0bc0-417b-abb3-a59df781f3a8)(the new index.html file has been uploaded)
![image](https://github.com/RamakrishnaVenkat/Techplement/assets/91265544/59b40a92-f575-40c5-964a-6376150a2938)(now the index.html file is open for being viewed by all)
![image](https://github.com/RamakrishnaVenkat/Techplement/assets/91265544/f0da9c14-e9ee-483e-afce-49bf8c2eb982)(a simple counter app has been created )









