# Upload Image with Javascript
---
Simple layout before you select the image you want to upload

![Output](layout_before_upload.png)

After selection of image from the local storage

![Output](layout_after_upload.png)

Javascript code to user

```javascript
let profilePic = document.getElementById("profile");
        let uploadPic = document.getElementById("upload");

        uploadPic.onchange = function(){
            profilePic.src = URL.createObjectURL(uploadPic.files[0])
        }