## How to setup the Integration of LinkedIn API with OAuth?

Hi everyone, I have recently worked on a project where we need to sync the user data using linkedIn, so to set up a sign in via LinkedIn I visited the LinkedIn developer documentation but there are no clear instructions, so I want the explain how can you set up easy login or sync user data through LinkedIn API.

* Many of us may have encountered on different websites, where you can log in with Facebook, Github, Google, and LinkedIn. These are operations are called the OAuth authorization setup. They are very similar to each other and everyone follows the same way. so now I going to explain setting up OAuth with linkedIn. This is the OAuth flow for the application 


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1599444635045/nvLNSwwHP.png)

Steps:

*  Visit the LinkedIn [developers website](https://www.linkedin.com/developers/) from your profile and now you will be able to see a create app button on the main page click on it.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598762877198/gtAZSX_mS.png)

*  After clicking on the page you will be able to see this page where you need to specify the app name, you have to enter the LinkedIn page name of the company which you will be associating the with the application you are building, enter any Privacy policy URL for your associated application, upload the company logo and create the application. 

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598763028307/mZoczMEag.png)

*  After that, you will be given a client id and client secret which we will be using later in your application in the Auth tab of the next page, here you also need to specify the redirect URL, which will be used to redirect to your application after login. 

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598763673930/Jjx65u_Wi.png)

 * Now  the main step is to get the data required for your application, for this, you need to have access to the user profile scopes such as r_basicprofile,r_fullprofile, and r_emailaddress, these are field which you will be able to access from the LinkedIn API which will be added based on the products you add in your application 

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598770936187/Hu_Bl1Mse.png)

* Now you need to configure the products for your application, the image below you need to select sign in with LinkedIn product so that u will get the basic profile and email address from the logged-in user. If you need to get all the user-related education, any other you need to set up other products or you need to apply for the different [partnership programs](https://developer.linkedin.com/partner-programs/apply) with LinkedIn to get the user full details.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598770801452/m-pOzi_e-.png)

* I have added the sign in with the LinkedIn product for my application which will get me r_liteprofile and r_emailaddress in your scopes.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1599407717691/iI6o0pujv.png)


#### I have created a react application with Nextjs and serverless functions for this use case. This is the sample [website](https://linkedin-oauth-example.vercel.app/). I have created which will get you your profile name and profile picture.

References:

LinkedIn developers URL: https://www.linkedin.com/developers/

Repo Link: https://github.com/sridhar02/LinkedIn-OAuth-example

sample website link: https://linkedin-oauth-example.vercel.app/

LinkedIn Documentation : https://docs.microsoft.com/en-us/linkedin/shared/authentication/authorization-code-flow?context=linkedin/compliance/context

> If you have any doubts related to this article or anything related to tech or software-engineering in general, drop a comment here or you can message me on twitter [@ksridhar02](https://twitter.com/ksridhar02).
 

