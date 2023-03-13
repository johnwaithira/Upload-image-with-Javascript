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


Javascript code

```javascript
let profilePic = document.getElementById("profile");
let uploadPic = document.getElementById("upload");
uploadPic.onchange = function(){
    profilePic.src = URL.createObjectURL(uploadPic.files[0])
}
```

CSS styling

```css
.container{
    width: 100%;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #ddd;
}
.card{
    width: 400px;
    background: #fff;
    padding: 40px;
    text-align: center;
    border-radius: 15px;
}
.card h1{
    padding: 10px 0;
}
.card img{
    width: 180px;
    height: 180px;
    border-radius: 100px;
    margin-top: 20px;
    margin-bottom: 20px;
}
input{
    display: none;
}
label{
    width: 180px;
    display: block;
    background: green;
    color: #fff;
    padding: 10px 20px;
    margin: 10px auto;
    border-radius: 10px;
}
```