index.html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Men T-Shirt Store</title>

<style>
body{
  margin:0;
  background:#111;
  font-family:Arial;
  color:white;
}

header{
  text-align:center;
  padding:25px;
  font-size:32px;
  font-weight:900;
  letter-spacing:2px;
}

.grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:12px;
  padding:12px;
}

.card{
  background:#1c1c1c;
  border-radius:12px;
  overflow:hidden;
  text-decoration:none;
  color:white;
}

.card img{
  width:100%;
  height:160px;
  object-fit:cover;
  display:block;
}

.name{
  text-align:center;
  padding:6px;
}

.price{
  text-align:center;
  padding-bottom:10px;
  font-weight:bold;
}
</style>
</head>

<body>

<header>MEN T-SHIRT</header>

<div class="grid">

<script>
const products = [
{n:"Black Wave",p:999},
{n:"Urban Grey",p:799},
{n:"Street King",p:899},
{n:"Dark Shadow",p:1099},
{n:"White Classic",p:699},
{n:"Night Rider",p:950},
{n:"Minimal Black",p:999},
{n:"Grey Force",p:850},
{n:"Alpha Wear",p:1200},
{n:"Storm Fit",p:899},
{n:"Neo Street",p:999},
{n:"Bold Edge",p:1050}
];

for(let i=0;i<products.length;i++){
document.write(`
<a class="card" href="product.html?id=${i}">
<img src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab">
<div class="name">${products[i].n}</div>
<div class="price">Rs.${products[i].p}</div>
</a>
`);
}
</script>

</div>

</body>
</html>

product.html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Product</title>

<style>
body{
  margin:0;
  background:#0f0f0f;
  font-family:Arial;
  color:white;
  text-align:center;
}

h1{
  font-size:34px;
  margin-top:20px;
}

img{
  width:90%;
  max-width:400px;
  border-radius:15px;
  margin-top:15px;
}

.price{
  font-size:28px;
  margin-top:10px;
  font-weight:bold;
}

.order{
  display:inline-block;
  margin-top:20px;
  padding:16px 30px;
  background:#25D366;
  color:white;
  font-weight:bold;
  text-decoration:none;
  border-radius:12px;
  font-size:18px;
}

.details{
  margin-top:25px;
  font-size:15px;
  color:#bbb;
  padding:0 20px;
  line-height:1.7;
}

.footer{
  margin-top:35px;
  border-top:1px solid #333;
  padding-top:15px;
  font-size:14px;
  color:#888;
}
</style>
</head>

<body>

<h1 id="name"></h1>

<img src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab">

<div class="price" id="price"></div>

<a class="order" id="wa" target="_blank">
📲 ORDER ON WHATSAPP
</a>

<div class="details">
Premium branded oversized men’s T-shirt collection.<br>
High quality cotton fabric, luxury streetwear design.<br>
Comfortable fit, long lasting print, premium fashion style.
</div>

<div class="footer">
📍 maggona main street <br>
📞 0754668668 <br><br>

<b>Terms & Policy</b><br>
No refund after use. Exchange within 24 hours only.
</div>

<script>
const products = [
"Black Wave","Urban Grey","Street King","Dark Shadow",
"White Classic","Night Rider","Minimal Black","Grey Force",
"Alpha Wear","Storm Fit","Neo Street","Bold Edge"
];

const prices = [999,799,899,1099,699,950,999,850,1200,899,999,1050];

const id = new URLSearchParams(window.location.search).get("id");

document.getElementById("name").innerText = products[id];
document.getElementById("price").innerText = "Rs. " + prices[id];

// REAL WHATSAPP FIX
const phone = "94754668668";

const msg = `Hello, I want to order:
Product: ${products[id]}
Price: Rs.${prices[id]}`;

document.getElementById("wa").href =
"https://wa.me/" + phone + "?text=" + encodeURIComponent(msg);
</script>

</body>
</html>
