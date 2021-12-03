# Device

Device includes several possible calls that provide information about the devices associated with an account. Does not appear to be limited to myTouchSmart and may include other Jasco brands like Enbrighten.

## List
----
List all devices associated with an account

### URL

  `https://myts.yunext.com/api/app/device/list`

### Method

`GET`
  
### URL Parameters


Required:

- `token=[token]`

### Success Response

Code: 600 <br/>
Content:
```
{
    "code": 600,
    "data": [
        {
            "macAddress": "MAC_ADDRESS",
            "companyCode": "02",
            "deviceType": "A4",
            "authCode": "29008",
            "deviceName": "Name of Device 1",
            "imageName": "",
            "orderNumber": 1,
            "lastOperation": UNIX_TIME,
            "cityId": "CITY_ID",
            "zoneId": "America/Time_zone",
            "gmtOffset": -300,
            "longtitude": DECIMAL,
            "latitude": DECIMAL,
            "version": null,
            "groupId": "GROUP_GUID",
            "gColorType": 1,
            "online": true
        },
        {
            "macAddress": "MAC_ADDRESS",
            "companyCode": "02",
            "deviceType": "A4",
            "authCode": "29008",
            "deviceName": "Name of Device 2",
            "imageName": "",
            "orderNumber": 1,
            "lastOperation": UNIX_TIME,
            "cityId": "CITY_ID",
            "zoneId": "America/Time_zone",
            "gmtOffset": -300,
            "longtitude": DECIMAL,
            "latitude": DECIMAL,
            "version": null,
            "groupId": "GROUP_GUID",
            "gColorType": 1,
            "online": true
        }
    ],
    "success": true
}
```
 
### Error Response

Code: 612 <br />
Content:
```
{
    "msg": "login again",
    "code": 612,
    "success": false
}
```

### Sample Call

`curl -d "token=token" https://myts.yunext.com/api/app/device/list`

## Notes

### URL Parameters

The required token for this `GET` is the same token returned by the [Service Login](https://ericlauber.github.io/myTouchSmart-Switch-Documentation/service/) `POST`.