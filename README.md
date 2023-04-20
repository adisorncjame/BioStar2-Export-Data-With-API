# api-swagger-biostar2-2.8.14

- Offline Swaggers
Those who have downloaded BioStar 2.8.14(or above) can go to the folder below to see the offline Swagger:
*You can also download the attached zip file(swagger folder) to experience offline swagger.
C:\Program Files\BioStar 2(x64)\nginx\html\swagger
![image](https://user-images.githubusercontent.com/62010897/233255854-17c73653-926e-422e-8c2e-7190d090c6d9.png)


How to access that Swagger of new API.
The way how to access the Swagger of the new API is changed from before. Please refer to the screenshot below.
  - [BioStar 2 address] + '/swagger/index.html'
    eg,) BioStar 2 address> https://192.168.16.35:456
           New BioStar 2 API Swagger> https://192.168.16.35:456/swagger/index.html
![image](https://user-images.githubusercontent.com/62010897/233255963-505e60a8-c2ef-4edf-9a96-cd1081b7d9e7.png)


Also, there are 2 main differences between the old API Swagger and the new API.

1. Need to additional save cookie information after login.

  > How to save cookie information? 

Success to login using the API that '[POST] /api/login'.

![image](https://user-images.githubusercontent.com/62010897/233256086-b7398948-91ed-4125-b19c-aaffe746388a.png)
![image](https://user-images.githubusercontent.com/62010897/233256110-07ea91e1-0583-4c22-a102-9568d0f92dce.png)

Get the cookie from the response.

![image](https://user-images.githubusercontent.com/62010897/233256132-05e196cd-5ede-4b0a-a5c9-38838171bb69.png)

Click the button named 'Authorize'

![image](https://user-images.githubusercontent.com/62010897/233256152-f81aa06c-01f6-479a-ba4c-20397d605efb.png)

Save the result of the cookie that you get from the response.

![image](https://user-images.githubusercontent.com/62010897/233256175-9629a145-0e6d-4e57-9d71-19d6cebaaa0b.png)


If you are the success that saves the cookie, you can find the lock icon's share is changed.

![image](https://user-images.githubusercontent.com/62010897/233256196-309b7c91-12fc-4f42-aa56-1545721dd6fd.png)


2. Expanded that available features with API
Before in the old API, the API supported the restricted features of BioStar 2's AC. 
But, the new API supports all of BioStar 2's AC features. For more information, please refer to the new API Swagger.


* If you are using port 443 to connect BioStar 2, please click the below link to connect to the new API Swagger.
LOCAL ADDRESS API > : https://127.0.0.1/swagger/index.html


LOGIN REQUIRED error - Session is expired

NOTE: The BioStar 2 Local API Server/BioStar 2 Web API are discontinued, this article is for reference only. For new developments please use the BioStar 2 API (version 2.9.x and later). 
If you have already logged in but see the LOGIN REQUIRED ACB_ERROR_CODE.10 when calling another API function you may not be managing the sessions properly.

![image](https://user-images.githubusercontent.com/62010897/233256480-e3f99a3d-14e8-4f1c-bfe8-4e136ed9f0e8.png)

All API calling users have to create a routine for session invalidation. 
Below are cases where sessions are invalid: 
1. A new login is made every time because the API is misused.
2. The server is restarted often.
3. Cookie value is not refreshed or not updated. 
4. A session timeout happens.


Config POSTMAN Test Api BioStar 2

[ Login Get bs-session-id ]

![image](https://user-images.githubusercontent.com/62010897/233257409-d6ce677a-63e2-40c3-867d-9e4a9f73183a.png)

![image](https://user-images.githubusercontent.com/62010897/233257380-7f15782f-161d-40df-b5e3-469029a04db9.png)

![image](https://user-images.githubusercontent.com/62010897/233257158-5ff506db-e3ed-4685-8a47-3e9f3296a3fa.png)

Copy > bs-session-id

[ Get Event Logs ]

![image](https://user-images.githubusercontent.com/62010897/233257662-fad9f15d-8a26-4b07-bebc-1fd9fcc187cc.png)

![image](https://user-images.githubusercontent.com/62010897/233257614-49b0aac8-0029-4b14-8030-e43d7e8ef904.png)


HTTPS ERROR STATUS > https://developer.mozilla.org/en-US/docs/Web/HTTP/Status#information_responses








