# Sun

Provides sunrise and sunset information.

## Info
----
Get the date information.

### URL

  `https://myts.yunext.com/api/app/sun/info`

### Method

`GET`

### URL Parameters

Required:

- `date=[YYYY-MM-DD]`

- `cityID=[CITY_ID]`

### Success Response

Code: 600 <br/>
Content:
```
{
    "code": 600,
    "data": {
        "sunrise": 1638449042,
        "sunset": 1638482762
    },
    "success": true
}
```

### Error Response

Code: 622 <br/>
Content:
```
{
    "msg": "app operated unsuccessfully",
    "code": 622,
    "success": false
}
```

### Sample Call

`curl -d "date=2021-12-01&cityID=CITY_ID" https://myts.yunext.com/api/app/sun/info`


## Notes

I've gotten successfully used `GET` to retrieve this data in Postman but have an error in the cURL command. cURL is defaulting to `POST`. I'm new to cURL and need to specify to use `GET`.

I have observed that it's possible to get an error response by providing an older date, such as one year ago.