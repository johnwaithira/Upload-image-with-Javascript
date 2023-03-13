# Upload Image with Javascript
---
Simple layout before you select the image you want to upload

![Output](layout_before_upload.png)

After selection of image from the local storage

![Output](layout_after_upload.png)

HTML code
```html
    <div class="container">
        <div class="card">
            <h1>Elon Musk</h1>
            <p>@elonmusk</p>
            <img src="/images/profile.png" id="profile">
            <label for="upload">Update Profile</label>
            <input type="file"  id="upload">
        </div>
    </div>
```    


Javascript code to user

```javascript
let profilePic = document.getElementById("profile");
let uploadPic = document.getElementById("upload");
uploadPic.onchange = function(){
    profilePic.src = URL.createObjectURL(uploadPic.files[0])
}
```