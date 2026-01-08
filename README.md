<h1>Creating an Amazon S3 Bucket</h1>

This project outlines the creation of an Amazon S3 bucket.<br />

<h2>Environments and Technologies Used</h2>

- AWS
- Amazon S3

<h2>Operating Systems Used</h2>

- Windows 11 Enterprise

<h2>High-Level Deployment and Configuration Steps</h2>

- Create the following Amazon S3 bucket: `kk-lab-chaan-s3`
    - The bucket should have `us-east-1` region
    - Ensure that the public access is disabled
- Upload the `food/` and `travel/` directories to the `kk-lab-chaan-s3` bucket
    - Ensure that the storage class is set to `Standard`
- Navigate to the food folder that was uploaded in the bucket.
- Select one of the JPG files and click on it.
- Then, click on the object URL link. As Access Denied XML response should be encountered.
- Next, return to the bucket view and click on the Open tab located in the top right section of the console. This action should successfully display the image.
- This behavior occurs because the object URL displays Access Denied due to it being a public link, while the S3 object JPG uploaded is private, as the Block all public access setting is enabled.
- The Open button functions correctly because you are logged into the AWS console, which uses your authenticated AWS permissions to access the object.
- Create a lifecycle policy named travel-lifecycle-policy that applies to all files within the travel directory of the bucket. Configure the policy settings as follows:
    - Under Lifecycle Action Rules, enable the Transition current versions of objects between storage classes.
    - Under the Transition current versions of objects between storage classes, move the current version from Standard-IA and transition to Glacier Instant Retrieval after 30 days.
- Delete the bucket with the prefix `kk-lab-chaan-s3`





<br />

<h1>Actions and Observations</h1>

## Creating the S3 Bucket
### In the AWS console home menu screen, click on S3 
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/41fc9bf0-a65d-4676-8368-d968fe668c36" />
</p>

### Click on "Create bucket"
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/8888813a-7217-400f-a12e-35a4ae819049" />
</p>

### To store objects across different availability zones and to have access to a wider ranger of storage classes, the bucket type will be set to `General Purpose`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/5b9b4cc6-1a4a-4254-b7e1-adf4560ccf19" />
</p>

### Give the name of the bucket as the following: `kk-lab-chaan-s3`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/af1172d7-4c16-402d-af31-8eed58ebc998" />
</p>

### To make this bucket accessible to only my accoint, ACLs will be disabled
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/1cdd690b-f1c0-4f82-9916-ccb7302a3fc6" />
</p>

### To make the bucket private for my account and not to the public, public access will be blocked for this bucket
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/523d48c9-4435-4233-a66a-b8af22b809f8" />
</p>

### Disable Bucket versioning as this will be the only version of this bucket
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/13d75b53-ce0a-422e-b576-2f6dfac0f21e" />
</p>

### Leave all other options as default
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/2a04328a-a0fa-44af-aea8-f261194729e3" />
</p>

### Create the bucket
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/044d734f-7cd6-4ab7-8cda-35d2d691ca9b" />
</p>

### Verify the created bucket
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/7ab5cecb-4587-4ec0-9fba-d1f4f9af82de" />
</p>
<br />

## Uploading files in the bucket
### Click on the bucket then click on "upload"
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/7ab5cecb-4587-4ec0-9fba-d1f4f9af82de" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/a99fdae2-61d3-4cef-a8e0-daf589d82ee6" />
</p>

### Click on "Add folder" in the Upload UI
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/71b45df5-2186-40ac-aeed-7503b4aabe4c" />
</p>

### Navigate to the location of the saved folder
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/eb03b8d5-5b73-468a-a390-3c1628c1c7d0" />
</p>

### Upload both the `food` directory
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/d03dd536-9ac5-4bb7-88ce-90467122cc0d" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/e0d40b78-dd6e-47b4-827e-3bf91ed7b9dc" />
</p>

### Upload both the `travel` directory
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/14faf8c3-9692-4c4b-9ee8-391c1b8d9721" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/6a84c994-2866-42d9-b76e-39f14c7c49e9" />
</p>

### Click "Upload" to upload the files into the bucket
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/d2f078a6-7672-4487-8664-d5dce6389f66" />
</p>

### Veriy that the files were uploaded
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/570e1691-6089-4c59-bc6e-f6e1d640adbf" />
</p>

### Navigate to the food directory
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/86251859-64a1-4ebc-b83e-3569d298bfd1" />
</p>
<br />

### Click on a image
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/6285a0f0-7e96-48a1-b8d3-00bbcd8451ef" />
</p>

### Click on the image URL to view the image, instead of the image showing, the Access denied XML response will appear, this is due to the public access being blocked during the creation of the `kk-lab-chaan-s3` bucket
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/9ebf0f66-3cb4-403c-9d8a-8d7074f45e2b" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/ea22ee1d-810d-4771-89a6-4cfb64de4ac0" />
</p>
<br />

### To view the Image, click on the "Open" hyperlink
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/1eec5768-b540-40fb-9838-7e3389ab3753" />
</p>

### 
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/2d3233e8-43ea-466c-b7dd-d5b2e74b3242" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/852a75ec-743e-4450-91c0-b900a69f3930" />
</p>
<br />

## Verifying the Users
### Verify the `Help Desk` user — this account should be part of the same groups as the `Administrator`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/4aaae8c4-a256-4a36-949d-113954d022a6" />
</p>
<br />

### Verify the user `Patty`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/45f46d96-8ac1-4db3-b5a7-e3e3b8e09f74" />
</p>
<br />

### Verify the user `Jane Foster`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/ad32724d-864d-4b80-8f9b-da7f501c2e9a" />
</p>
<br />

### Verify the user `Jamie Verges`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/7adbee0b-fc4b-49e0-9452-4c083b691e58" />
</p>
<br />

### Verify the user `Eric Madson`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/72afb1c9-47dc-4ad2-9c33-13d3063423df" />
</p>
<br />

### Verify the user `Alex Bertzy`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/5c8da4e1-c49e-44f2-bf0d-d6bf276f2641" />
</p>

---

<br />

# End of Project


