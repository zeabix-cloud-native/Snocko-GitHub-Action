# Readme for Disable or Enable Github actions Workflows

## Prerequisite

### 1. Create PAT (Personal Access Token)

1. In the upper-right corner of any page, click your profile photo, then click **Settings.**

![image](https://user-images.githubusercontent.com/46469458/206351284-2bb410a9-8b31-4509-8462-4610521ad9ca.png)

2. In the left sidebar, click **Developer settings.**

![image](https://user-images.githubusercontent.com/46469458/206351454-5d50fdc1-3675-4a68-ad27-d75bc2c3988b.png)

3. In the left sidebar, click **Personal access tokens. --> Tokens (classic)**

<img width="1157" alt="image" src="https://user-images.githubusercontent.com/46469458/206352244-321c235f-2915-4096-b056-270ad233db50.png">

4. Click **Generate new token.**

![image](https://user-images.githubusercontent.com/46469458/206351650-a4c924a3-6b4a-4653-8ade-cbe4f6fc4209.png)

5. Enter : `CD_PAT`

<img width="478" alt="image" src="https://user-images.githubusercontent.com/46469458/206353702-53fdead9-810f-49db-8faf-f67737c8ce21.png">

6. To give your token an expiration, select the **Expiration** drop-down menu, then click a default or use the calendar picker.

![image](https://user-images.githubusercontent.com/46469458/206351769-7ec7c0a2-068c-4d6a-8982-4cdb37dd84e7.png)

7. Select the scopes.

<img width="827" alt="image" src="https://user-images.githubusercontent.com/46469458/206353356-242db48b-1f5f-4eb9-94dc-e21c148ce500.png">

8. Click **Generate token.**

![image](https://user-images.githubusercontent.com/46469458/206353540-4c932426-26fc-415a-8049-3769d56a72c0.png)

---
Reference : https://docs.github.com/en/enterprise-server@3.4/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

## disable-circleci.yml

### Run this workflows when you disabled circleci and want to enable github actions

1. Change repository name in `repo.txt` (Optional)

<img width="225" alt="image" src="https://user-images.githubusercontent.com/46469458/206343586-157c4e1d-b07b-4de5-af6a-5466ef300cd5.png">

2. Run this workflows **after disable circleci workflows and before commit file to github** to enable github actions workflows

<img width="1512" alt="image" src="https://user-images.githubusercontent.com/46469458/206343090-5afe003e-8531-4257-87fc-bca586687946.png">

3. commit file to github to run github actions workflows 

#### Explain code 

<img width="502" alt="image" src="https://user-images.githubusercontent.com/46469458/206356687-3b0a0714-4891-4653-8fe5-1f8847dc6c77.png">
<img width="483" alt="image" src="https://user-images.githubusercontent.com/46469458/206620473-20b328e1-3d84-45a0-8ea1-3f42d42499c4.png">
<img width="574" alt="image" src="https://user-images.githubusercontent.com/46469458/206356754-a81a5051-a163-4e03-8a80-fa6fc669f9b0.png">
<img width="581" alt="image" src="https://user-images.githubusercontent.com/46469458/206356880-8f00ed6e-2292-4c7e-ac4d-829e46d838f2.png">
<img width="722" alt="image" src="https://user-images.githubusercontent.com/46469458/206383808-7f85208d-f779-476d-a094-9ee5792916b7.png">
<img width="690" alt="image" src="https://user-images.githubusercontent.com/46469458/206383881-8ebd632c-b49b-4e4f-8e31-1bdb62c03696.png">
<img width="786" alt="image" src="https://user-images.githubusercontent.com/46469458/206383939-ef200d66-e270-468d-8a93-cba87a8c9ef3.png">

---

## enable-circleci.yml

### Run this workflows when you enabled circleci and want to disable github actions

1. Change repository name in `repo.txt` (Optional)

<img width="225" alt="image" src="https://user-images.githubusercontent.com/46469458/206343586-157c4e1d-b07b-4de5-af6a-5466ef300cd5.png">

2. Run this workflows **after enable circleci workflows and before commit file to github** to disable github actions workflows

<img width="1494" alt="image" src="https://user-images.githubusercontent.com/46469458/206346321-6aa8bc40-329a-4154-9743-4f45dac4da4f.png">

3. commit file to github to run circleci workflows

#### Explain code 

<img width="502" alt="image" src="https://user-images.githubusercontent.com/46469458/206356687-3b0a0714-4891-4653-8fe5-1f8847dc6c77.png">
<img width="483" alt="image" src="https://user-images.githubusercontent.com/46469458/206620473-20b328e1-3d84-45a0-8ea1-3f42d42499c4.png">
<img width="752" alt="image" src="https://user-images.githubusercontent.com/46469458/206385100-c783b356-19da-46a6-8d5b-dcaad44aefb8.png">
<img width="697" alt="image" src="https://user-images.githubusercontent.com/46469458/206385603-78b9fe20-782d-4187-8b75-40100a51311e.png">
<img width="813" alt="image" src="https://user-images.githubusercontent.com/46469458/206385321-2f06180b-438d-4793-b758-be281b6eced1.png">




