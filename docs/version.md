# Version

Version appears to provide access to files for different kinds of devices. Based on the results, these look like they may be firmware binaries.

## List
----
List out the details.

### URL

  `https://myts.yunext.com/api/app/version/list`

### Method

`GET`

### Success Response

Code: 600 <br/>
Content:
```
{
    "code": 600,
    "data": [
        {
            "deviceType": "A5",
            "version": "1.14",
            "url": "http://myts.yunext.com/uploadedFile/NW2661_MTLK(D)_upgrade_ver-1.14_20190613.bin"
        },
        {
            "deviceType": "B1",
            "version": "0.1",
            "url": "http://userdata.link2home.com/uploadedFile/lpt120-main_upgrade_B1_0.1_20180615.bin"
        },
        {
            "deviceType": "",
            "version": "",
            "url": "http://myts.yunext.com/uploadedFile/"
        },
        {
            "deviceType": "D2",
            "version": "1.06",
            "url": "http://userdata.link2home.com/uploadedFile/NW2034_UPGRADE_HSF_HDG_L2H_D2_V1.06_20180629.bin"
        },
        {
            "deviceType": "A2",
            "version": "2.07",
            "url": "http://myts.yunext.com/uploadedFile/UPGRADE_HSF_HDG_HAIDA_MYTS_A2_V2.07_20190410.bin"
        },
        {
            "deviceType": "A3",
            "version": "2.3",
            "url": "http://myts.yunext.com/uploadedFile/NW1703_UPGRADE_LPT220_MTLK_15R-2.3_20190424.bin"
        },
        {
            "deviceType": "A4",
            "version": "1.18",
            "url": "http://userdata.link2home.com/uploadedFile/NW1703_UPGRADE_LPT220_MTLK_15S_1.14_20180725.bin"
        },
        {
            "deviceType": "A1",
            "version": "2.07",
            "url": "http://myts.yunext.com/uploadedFile/UPGRADE_HSF_HDG_HAIDA_MYTS_A1_V2.07_20190329.bin"
        },
        {
            "deviceType": "D1",
            "version": "1.10b",
            "url": "http://userdata.link2home.com/uploadedFile/NW2034_UPGRADE_HSF_HDG_L2H_D1_V1.10b_20180619.bin"
        },
        {
            "deviceType": "E1",
            "version": "0.6",
            "url": "http://userdata.link2home.com/uploadedFile/LPT100FS2W_UPGARDE_20180704_0.6.bin"
        }
    ],
    "success": true
}
```

### Sample Call

`curl -d "token=token" https://myts.yunext.com/api/app/version/list`

## Notes

At this time, we lack information on which `deviceType` corresponds with actual products sold by Jasco, however the filenames provided may be a clue.