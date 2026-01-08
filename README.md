<h1>Creating a Bucket within Amazon S3</h1>

This project outlines the creation of an Amazon S3 bucket.<br />

<h2>Environments and Technologies Used</h2>

- AWS
- Amazon S3

<h2>Operating Systems Used</h2>

- Windows 11 Enterprise

<h2>High-Level Deployment and Configuration Steps</h2>

- Create the following Amazon S3 bucket: `kk-lab-chaanyah-s3`
    - The bucket should have `us-east-1` region
    - Ensure that the public access is disabled
- Upload the `food/` and `travel/` directories to the `kk-lab-chaaanyah-s3` bucket
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
- Delete the bucket with the prefix `kk-lab-chaanyah-s3`





<br />

<h1>Actions and Observations</h1>

## Creating the S3 Bucket
### In the AWS console home menu screen, click on S3 
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/41fc9bf0-a65d-4676-8368-d968fe668c36" />
</p>
<br />

### Click on "Create bucket"
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/8888813a-7217-400f-a12e-35a4ae819049" />
</p>
<br />

### To store objects across different availability zones and to have access to a wider ranger of storage classes, the bucket type will be set to `General Purpose`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/5b9b4cc6-1a4a-4254-b7e1-adf4560ccf19" />
</p>

### Give the name of the bucket as the following: `kk-lab-chaanyah-s3`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/b44f5cdd-a88b-4c91-be83-6bf5b0b93bbe" />
</p>

### To make this bucket accessible to only my accoint, ACLs will be disabled
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/1cdd690b-f1c0-4f82-9916-ccb7302a3fc6" />
</p>

### To make the bucket private for my account and not to the public, public access will be blocked for this bucket
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/523d48c9-4435-4233-a66a-b8af22b809f8" />
</p>
<br />

## Creating the Users
### Create the following users: `Help Desk`, `Patty`, `Jane Foster`, `Jamie Verges`, `Eric Madson`, and `Alex Bertzy`
For the `Help Desk` user, provide a secure password and set it to never expire.  
For the remaining users, set a temporary password that requires them to change it upon first login.
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/7461cc8f-d996-4ccc-a0b9-95b06b21bb34" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/3099bbd6-1d22-43e1-86ef-2a9e44947716" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/e4b6fc9f-6fd9-40d2-af2c-91d6e5a831dc" />
</p>
<br />

### Creating the user `Patty`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/47a4c0a9-ce06-4d45-84ce-a1ce2d4d1c05" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/bc0cd0d9-3098-44b2-9eb7-d765eb842a3d" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/2d50adde-9062-4a2e-8394-b15ef34da712" />
</p>
<br />

### Creating the user `Jane Foster`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/cc6a7e15-5b4c-4c1a-ab6c-6660d093fd15" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/0dbe713a-b1b5-4ed7-abad-948f4e303121" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/13ac8a97-c4f4-4e98-a967-35101d12e4a9" />
</p>
<br />

### Creating the user `Jamie Verges`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/f8389eac-ac89-403b-9e57-9a46de099c40" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/2d3233e8-43ea-466c-b7dd-d5b2e74b3242" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/7794e206-3057-4a6a-bae6-2b32cf01766e" />
</p>
<br />

### Creating the user `Eric Madson`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/3779d94f-27ba-41fe-a72e-ebd026e54b74" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/2d3233e8-43ea-466c-b7dd-d5b2e74b3242" />
</p>
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/b8fb9a18-f432-4cf4-9dff-882e2595d860" />
</p>
<br />

### Creating the user `Alex Bertzy`
<p>
<img width="550" height="550" alt="image" src="https://github.com/user-attachments/assets/8a6f6e9c-822a-4052-ba1d-c1361bd34f94" />
</p>
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


