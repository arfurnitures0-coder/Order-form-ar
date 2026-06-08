```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AR Furnitures | Luxury Order Form</title>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Inter',sans-serif;
}

body{
min-height:100vh;
display:flex;
align-items:center;
justify-content:center;
padding:40px 20px;
background:
radial-gradient(circle at top left,#222 0%,#000 40%),
radial-gradient(circle at bottom right,#111 0%,#000 50%);
overflow-x:hidden;
}

body::before{
content:'';
position:fixed;
width:500px;
height:500px;
border-radius:50%;
background:rgba(255,255,255,0.04);
top:-150px;
left:-150px;
filter:blur(80px);
}

body::after{
content:'';
position:fixed;
width:500px;
height:500px;
border-radius:50%;
background:rgba(255,255,255,0.03);
bottom:-150px;
right:-150px;
filter:blur(100px);
}

.form-card{
width:100%;
max-width:850px;

background:rgba(255,255,255,0.08);
backdrop-filter:blur(25px);
-webkit-backdrop-filter:blur(25px);

border:1px solid rgba(255,255,255,0.12);
border-radius:30px;

padding:50px;

box-shadow:
0 30px 80px rgba(0,0,0,.55),
inset 0 1px 0 rgba(255,255,255,.12);
}

.logo-area{
text-align:center;
margin-bottom:40px;
}

.logo-box{
width:90px;
height:90px;
margin:auto;
border-radius:24px;

background:linear-gradient(
145deg,
rgba(255,255,255,.16),
rgba(255,255,255,.04)
);

border:1px solid rgba(255,255,255,.15);

display:flex;
align-items:center;
justify-content:center;

font-size:34px;
font-weight:700;
color:#fff;

margin-bottom:20px;
}

.logo-area h1{
font-size:34px;
font-weight:700;
letter-spacing:4px;
color:#fff;
}

.logo-area p{
color:rgba(255,255,255,.65);
margin-top:10px;
font-size:14px;
letter-spacing:1px;
}

.section{
margin-top:30px;
}

.section-title{
color:#fff;
font-size:14px;
letter-spacing:2px;
font-weight:600;
margin-bottom:18px;
text-transform:uppercase;
}

.grid{
display:grid;
grid-template-columns:1fr 1fr;
gap:20px;
}

.field{
display:flex;
flex-direction:column;
}

.field.full{
grid-column:1/-1;
}

label{
color:rgba(255,255,255,.85);
font-size:13px;
margin-bottom:10px;
font-weight:500;
}

input,
textarea{
width:100%;
padding:16px 18px;

background:rgba(255,255,255,.05);
border:1px solid rgba(255,255,255,.12);

border-radius:16px;

color:#fff;
font-size:14px;

transition:.35s ease;
}

input::placeholder,
textarea::placeholder{
color:rgba(255,255,255,.35);
}

input:focus,
textarea:focus{
outline:none;

border-color:rgba(255,255,255,.45);

background:rgba(255,255,255,.08);

box-shadow:
0 0 0 4px rgba(255,255,255,.05);
}

textarea{
resize:vertical;
min-height:120px;
}

.upload-box{
padding:25px;
border:2px dashed rgba(255,255,255,.18);
border-radius:18px;
text-align:center;
background:rgba(255,255,255,.03);
}

.upload-box input{
border:none;
background:none;
padding:0;
}

.submit-btn{
width:100%;
margin-top:35px;

padding:18px;

border:none;
border-radius:18px;

background:linear-gradient(
180deg,
#ffffff,
#d7d7d7
);

color:#000;
font-size:15px;
font-weight:700;
letter-spacing:2px;

cursor:pointer;
transition:.35s ease;
}

.submit-btn:hover{
transform:translateY(-3px);

box-shadow:
0 15px 35px rgba(255,255,255,.18);
}

.submit-btn:active{
transform:scale(.98);
}

.footer-note{
margin-top:20px;
text-align:center;
color:rgba(255,255,255,.5);
font-size:12px;
}

@media(max-width:768px){

.form-card{
padding:30px 22px;
}

.grid{
grid-template-columns:1fr;
}

.logo-area h1{
font-size:26px;
}

}

</style>
</head>

<body>

<form class="form-card"
action="https://api.web3forms.com/submit"
method="POST"
enctype="multipart/form-data">

<input type="hidden"
name="access_key"
value="arfurnitures0@gmail.com">

<input type="hidden"
name="subject"
value="New Luxury Order Form Submission">

<div class="logo-area">

<div class="logo-box">
AR
</div>

<h1>AR FURNITURES</h1>

<p>
sofa and chair manufacturer 
</p>

</div>

<div class="section">

<div class="section-title">
Client Information
</div>

<div class="grid">

<div class="field">
<label> Name *</label>
<input type="text"
name="name"
required
placeholder="Enter Full Name">
</div>

<div class="field">
<label>GST Number </label>
<input type="text"
name="gst_number"
placeholder="GST Number">
</div>

<div class="field">
<label>Contact Number *</label>
<input type="tel"
name="phone"
required
placeholder="+91 XXXXX XXXXX">
</div>

<div class="field">
<label>Email Address *</label>
<input type="email"
name="email"
required
placeholder="name@company.com">
</div>

<div class="field full">
<label>Delivery Address *</label>
<textarea
name="address"
required
placeholder="Complete Delivery Address"></textarea>
</div>

<div class="field full">
<label>Product Requirement *</label>
<input type="text"
name="product"
required
placeholder="Product / Chair Model Name">
</div>

<div class="field full">
<label>Reference Image</label>

<div class="upload-box">
<input type="file"
name="attachment"
accept="image/*">
</div>

</div>

</div>

</div>

<button class="submit-btn" type="submit">
SUBMIT ORDER REQUEST
</button>

<div class="footer-note">
Luxury Workspace Solutions by AR Furnitures
</div>

</form>

</body>
</html>
```

