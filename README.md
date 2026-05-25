Mens store
<Mens store>
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
{n:"Plane white",p:950},
{n:"cocordile plane white",p:999},
{n:"white patch",p:850},
{n:"polo white gen",p:1200},
{n:"white Fit",p:899},
{n:"white loose",p:999},
{n:"POLO white",p:1050}
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
</Mens choice>
