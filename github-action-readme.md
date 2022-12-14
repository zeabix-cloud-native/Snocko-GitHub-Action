# Readme for Disable or Enable Github actions Workflows

## Prerequisite

### Create PAT (Personal Access Token) for github actions

1. In the upper-right corner of any page, click your profile photo, then click **Settings.**

![image](https://user-images.githubusercontent.com/46469458/206351284-2bb410a9-8b31-4509-8462-4610521ad9ca.png)

2. In the left sidebar, click **Developer settings.**

![image](https://user-images.githubusercontent.com/46469458/206351454-5d50fdc1-3675-4a68-ad27-d75bc2c3988b.png)

3. In the left sidebar, click **Personal access tokens. --> Tokens (classic)**

<img width="1157" alt="image" src="https://user-images.githubusercontent.com/46469458/206352244-321c235f-2915-4096-b056-270ad233db50.png">

4. Click **Generate new token.**

![image](https://user-images.githubusercontent.com/46469458/206351650-a4c924a3-6b4a-4653-8ade-cbe4f6fc4209.png)

5. Enter : `GH_CMD`

<img width="481" alt="image" src="https://user-images.githubusercontent.com/46469458/207613958-5711d1c0-84e4-49f0-a9de-076ecd4cb84d.png">

6. To give your token an expiration, select the **Expiration** drop-down menu, then click a default or use the calendar picker.

![image](https://user-images.githubusercontent.com/46469458/206351769-7ec7c0a2-068c-4d6a-8982-4cdb37dd84e7.png)

7. Select the scopes.

<img width="827" alt="image" src="https://user-images.githubusercontent.com/46469458/207614233-2790c230-87a8-4da8-b6c0-acff976154af.png">

8. Click **Generate token.**

![image](https://user-images.githubusercontent.com/46469458/206353540-4c932426-26fc-415a-8049-3769d56a72c0.png)

Reference : https://docs.github.com/en/enterprise-server@3.4/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

### Create PAT (Personal Access Token) for circleci

1. In the CircleCI application, go to your User settings.

<img width="252" alt="image" src="https://user-images.githubusercontent.com/46469458/207616312-c9da6d57-ca1c-4b07-9d2b-863e829410e3.png">

2. Click Personal API Tokens.

<img width="1390" alt="image" src="https://user-images.githubusercontent.com/46469458/207616438-78b35121-0245-4da3-86e2-76866aa18c6a.png">

3. Click the Create New Token button.

<img width="1025" alt="image" src="https://user-images.githubusercontent.com/46469458/207616590-8d840eb5-20bc-4e08-8bbe-2a3027cea5ac.png">

4. In the Token name enter: `CIRCLE_API_TOKEN` and Click the Add API Token button.

<img width="530" alt="image" src="https://user-images.githubusercontent.com/46469458/207616876-25171386-6294-448f-a313-c09291dee3d7.png">

5. After the token appears, copy and paste it to another location. You will not be able to view the token again.

Reference : https://circleci.com/docs/managing-api-tokens/#creating-a-personal-api-token

### Get your context id 

To prepare your context id please follow up this step

1. Go to Organization settings --> Contexts --> Click contexts name ` DisableEnable `

<img width="1404" alt="image" src="https://user-images.githubusercontent.com/46469458/207620178-b70f1e13-bb87-4449-8833-3b9248728977.png">

2. At URL please copy value 

Ex. https:// app.circleci. com/settings/organization/github/`{Your organization name}`/contexts/`b8a14bf5-4914-4e46-b0a6-e5abf21c944e`?return-to=https%3A%2F%2Fapp.circleci.com%2Fpipelines%2Fgithub%2F`{Your organization name}`

b8a14bf5-4914-4e46-b0a6-e5abf21c944e = context id

<img width="1391" alt="image" src="https://user-images.githubusercontent.com/46469458/207622028-08d8959a-d7f5-4921-8445-b2c0bd8edfeb.png">

3. Create github actions organization secret name : ` CIRCLECICONTEXTID ` and paste value from above

---
## switch-actions.yml

Run this workflow to enable or disabel both github actions and circleci

<img width="1481" alt="image" src="https://user-images.githubusercontent.com/46469458/207625737-1a00b814-a08f-4e6f-aa1d-2c568be1cf4c.png">

<img width="837" alt="image" src="https://user-images.githubusercontent.com/46469458/207625935-11458bfc-258b-4154-966e-5754fcc1dd1e.png">
<img width="744" alt="image" src="https://user-images.githubusercontent.com/46469458/207626032-c8c285b3-28a5-4ed3-b9a6-2dd0d9950b46.png">
<img width="841" alt="image" src="https://user-images.githubusercontent.com/46469458/207626294-c2e865f5-ae1f-4c88-828b-cce36184f10d.png">
<img width="805" alt="image" src="https://user-images.githubusercontent.com/46469458/207626895-9e38f367-7cdd-4f3a-8e74-32938727e740.png">
<img width="779" alt="image" src="https://user-images.githubusercontent.com/46469458/207627005-b58123c7-ead7-4a44-9359-dcf5662f5d6b.png">
<img width="896" alt="image" src="https://user-images.githubusercontent.com/46469458/207627162-c9b2ad69-b203-4393-82d8-aa52f2261038.png">
<img width="634" alt="image" src="https://user-images.githubusercontent.com/46469458/207627257-004bad9c-ce7a-4e54-960a-2e4aed566537.png">
<img width="821" alt="image" src="https://user-images.githubusercontent.com/46469458/207627756-c1985805-19fa-4347-b2f8-9917cfc08b3a.png">
<img width="656" alt="image" src="https://user-images.githubusercontent.com/46469458/207627853-ca914fe7-32bb-4e6a-9352-628a5c33f1a6.png">
<img width="838" alt="image" src="https://user-images.githubusercontent.com/46469458/207627950-31c0b439-b25d-4a18-afa9-f72c38932c25.png">

