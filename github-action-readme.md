# Readme for Disable or Enable Github actions Workflows

## Prerequisite

### Create PAT (Personal Access Token)

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

### Change organization owner name

1. Change  
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
<img width="574" alt="image" src="https://user-images.githubusercontent.com/46469458/206356754-a81a5051-a163-4e03-8a80-fa6fc669f9b0.png">
<img width="581" alt="image" src="https://user-images.githubusercontent.com/46469458/206356880-8f00ed6e-2292-4c7e-ac4d-829e46d838f2.png">
<img width="737" alt="image" src="https://user-images.githubusercontent.com/46469458/206357254-f43db9c0-abf2-426d-b161-53aa31db548f.png">
<img width="573" alt="image" src="https://user-images.githubusercontent.com/46469458/206357436-639d56e8-8065-4645-8324-0c8530ddaa83.png">
<img width="793" alt="image" src="https://user-images.githubusercontent.com/46469458/206357475-2f321c88-bb07-4c8a-bf1e-6e8db8b943bd.png">

---

## enable-circleci.yml

### Run this workflows when you enabled circleci and want to disable github actions

1. Change repository name in `repo.txt` (Optional)

<img width="225" alt="image" src="https://user-images.githubusercontent.com/46469458/206343586-157c4e1d-b07b-4de5-af6a-5466ef300cd5.png">

2. Run this workflows **after enable circleci workflows and before commit file to github** to disable github actions workflows

<img width="1494" alt="image" src="https://user-images.githubusercontent.com/46469458/206346321-6aa8bc40-329a-4154-9743-4f45dac4da4f.png">
