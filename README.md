<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Luxury Ride Deals – Car Inspection</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body{margin:0;font-family:Arial;background:#000;color:#fff}
header{text-align:center;padding:20px;background:#000}
header img{width:180px}
.price{font-size:22px;color:gold;margin:10px 0}
.section{padding:15px}
.section h2{border-bottom:1px solid gold;padding-bottom:5px}
.gallery{display:grid;grid-template-columns:repeat(auto-fill,minmax(120px,1fr));gap:10px}
.gallery img{width:100%;border-radius:8px}
.whatsapp{
position:fixed;bottom:20px;right:20px;
background:#25D366;color:#fff;
padding:15px;border-radius:50%;
font-size:22px;text-decoration:none
}
.admin{background:#111;padding:15px;margin:15px;border-radius:10px}
input,select,button{
width:100%;padding:10px;margin:5px 0;border-radius:5px;border:none
}
button{background:gold;color:#000;font-weight:bold}
</style>
</head>

<body>

<header>
<img src="https://i.imgur.com/9QZQZQp.png">
<h1>Luxury Ride Deals</h1>
<p>Pre-Owned Luxury, Perfected</p>
<div class="price">Price: ₹ <span id="price">--</span></div>
</header>

<div class="section">
<h2>Inspection Gallery</h2>
<div class="gallery" id="gallery"></div>
</div>

<a class="whatsapp" href="https://wa.me/917240801833" target="_blank">💬</a>

<div class="admin">
<h2>Add Car / Inspection (Admin)</h2>
<input id="imgurl" placeholder="Image URL">
<select id="type">
<option>Exterior</option>
<option>Interior</option>
<option>Engine</option>
<option>Damages</option>
<option>Video</option>
</select>
<input id="priceinput" placeholder="Car Price ₹">
<button onclick="addImage()">Add</button>
</div>

<script>
function addImage(){
let url=document.getElementById("imgurl").value;
let price=document.getElementById("priceinput").value;
if(price) document.getElementById("price").innerText=price;
let img=document.createElement("img");
img.src=url;
document.getElementById("gallery").appendChild(img);
}
</script>

</body>
</html>
