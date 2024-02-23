
# BookMySport

This project is about a platform which gives user a flexibility to book sports for a various location and helps service provider to get user based on the sports that are available within the premises of Service provider


# Authentication Repository

## API Reference

#### Add User or Service Provider

```http
  POST /api/adduser
```
**Header**
| Parameter | Type     | Description| 
| :-------- | :------- | :----------| 
| `role` | `string` | **Required**. It must be user or service provider 

**Body**
| Parameter | Type     | Description| 
| :-------- | :------- | :----------| 
| `userName` | `string` | **Required**. UserName of User or service provider
| `email` | `string` | **Required**. Email of user or service provider
| `phoneNumber` | `string` | **Required**. PhoneNumber of User or service provider
| `password` | `string` | **Required**. Password of User or service provider
| `address` | `string` | **Required for Service provider Only**. Address of service provider
| `centreName` | `string` | **Required for Service provider Only**. centreName of service provider
| `startTime` | `Int` | **Required for Service provider Only**. start time of playground
| `stopTime` | `Int` | **Required for Service provider Only**. start time of playground


#### Login User or Service Provider

```http
  GET /api/login
```

**Header**
| Parameter | Type     | Description| 
| :-------- | :------- | :----------| 
| `role` | `string` | **Required**. It must be user or service provider 

**Body**
| Parameter | Type     | Description| 
| :-------- | :------- | :----------| 
| `email` | `string` | **Required**. Email of user or service provider
| `password` | `string` | **Required**. Password of User or service provider

#### Two Factor Authentication User or Service Provider

```http
  POST /api/2fa
```

**Header**
| Parameter | Type     | Description| 
| :-------- | :------- | :----------| 
| `otpforTwoFAFromUser` | `string` | **Required**. It will get send to you when you will login using login api
| `role` | `string` | **Required**. user or service provider

#### Forgot Password User or Service Provider

```http
  POST /api/forgotpassword
```

**Header**
| Parameter | Type     | Description| 
| :-------- | :------- | :----------| 
| `email` | `string` | **Required**. provide Email Present in database 

#### Verify OTP for forgot password API User or Service Provider

```http
  POST /api/verifyOtpforforgotpassword
```

**Header**
| Parameter | Type     | Description| 
| :-------- | :------- | :----------| 
| `otp` | `string` | **Required**. provide OTP which will be sent to Email


#### Reset Password API User or Service Provider

```http
  POST /api/resetpassword
```

**Header**
| Parameter | Type     | Description| 
| :-------- | :------- | :----------| 
| `passwordFromUser` | `string` | **Required**. provide new Password to be sent
| `role` | `string` | **Required**. User or Service Provider

####  Search for Centre or Address for User 

```http
  GET /api/searchbyaddressandcentrename
```

**Header**
| Parameter | Type     | Description| 
| :-------- | :------- | :----------| 
| `searchItem` | `string` | **Required**. search for any address or centre name for results.

####  Search for Centre or Address for User 

```http
  PUT /api/updateplaygrounddetails
```

**Header**
| Parameter | Type     | Description| 
| :-------- | :------- | :----------| 
| `token` | `string` | **Required**. token for service provider or user 


**Body**
| Parameter | Type     | Description| 
| :-------- | :------- | :----------| 
| `phoneNumber` | `string` | **Required**. PhoneNumber of User or service provider
| `address` | `string` | **Required for Service provider Only**. Address of service provider
| `centreName` | `string` | **Required for Service provider Only**. centreName of service provider
| `startTime` | `Int` | **Required for Service provider Only**. start time of playground
| `stopTime` | `Int` | **Required for Service provider Only**. start time of playground 


####  Password Reset for User or Service Provider 

```http
  POST /api/updateplaygrounddetails
```

**Header**
| Parameter | Type     | Description| 
| :-------- | :------- | :----------| 
| `token` | `string` | **Required**. token for service provider or user 


**Body**
| Parameter | Type     | Description| 
| :-------- | :------- | :----------| 
| `phoneNumber` | `string` | **Required**. PhoneNumber of User or service provider
| `address` | `string` | **Required for Service provider Only**. Address of service provider
| `centreName` | `string` | **Required for Service provider Only**. centreName of service provider
| `startTime` | `Int` | **Required for Service provider Only**. start time of playground
| `stopTime` | `Int` | **Required for Service provider Only**. start time of playground 



## Authors

- [@Anandateertha](https://github.com/VortexProjects)

- [@Nikunj](https://github.com/nkthis)






