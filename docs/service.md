# Service

Service appears to provide access to information that is account-focused instead of device-focused.

## Log into myTouchSmart
----
Provide user credentials to myTouchSmart in order to generate a token used in subsequent calls.

### URL

  `https://myts.yunext.com/api/service/user/login/MYTS`

### Method

`POST`
  
### URL Parameters

Required:

- `username=[Email Address]`

- `password=[Encrypted String]`

Optional:

- `phoneType=[Model of Phone]`

- `appType=[Type of the calling application]`

- `appVersion=[Version of the calling application]`

- `sign=[sign]`

- `phoneSysVersion=[Android version]`

### Success Response

Code: 600 <br/>
Content:
```
{
  "code": 600,
  "data": {
      "token": "[token]"
  },
  "success": true
}
```
 
### Error Responses

Code: 400 <br />
Returns an Apache Tomcat/8.0.39 Error Report:

Content:
```
HTTP Status 400
The request sent by the client was syntactically incorrect.
Apache Tomcat/8.0.39
```

Code: 602 <br />
Content:
```
{
  "msg": "username or password error",
  "code": 602,
  "success": false
}
```

### Sample Call

For the required inputs:

- Username: YourAccount@domain.com

- Encrypted Password: SomePassword

`curl -d "username=YourAccount%40domain.com&password=SomePassword" https://myts.yunext.com/api/service/user/login/MYTS`

For the required and optional inputs:

- Username: YourAccount@domain.com

- Encrypted Password: SomePassword

- Phone Type: Pixel 5

- App Version: myTS 2.2

- App Type: 1

- Sign: 123XYZ

- Phone System Version: Android 12

  `curl -d "username=YourAccount%40domain.com&password=SomePassword&phoneType=Pixel%205&appVersion=2.2&appType=1&sign=123XYZ&phoneSysVersion=Android%3A12" https://myts.yunext.com/api/service/user/login/MYTS`

## Notes

### URL Parameters

At this time, the encryption algorithm and any key is unknown. The `sign` input is also unknown. Could it be the encryption key?

The App Version type appears to be an integer

Although some parameters are optional, changing their values, or choosing whether to include or exclude them will impact that token that the API returns.