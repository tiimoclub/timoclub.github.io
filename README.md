<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TIMO CLUB</title>

<style>
*{box-sizing:border-box;font-family:Arial}

body{
margin:0;
background:#000;
color:#fff;
text-align:center;
}

/* ===== اختيار الجنس ===== */
#genderGate{
min-height:100vh;
display:flex;
justify-content:center;
align-items:center;
position:relative;
overflow:hidden;
}

#genderBg{
position:absolute;
top:0;left:0;
width:100%;
height:100%;
object-fit:cover;
z-index:-2;
}

#overlay{
position:absolute;
top:0;left:0;
width:100%;
height:100%;
background:rgba(0,0,0,.65);
z-index:-1;
}

#genderBox{
background:rgba(0,0,0,.6);
padding:30px;
border-radius:16px;
}

.gender-btn{
width:240px;
padding:16px;
margin:12px 0;
font-size:20px;
border:none;
border-radius:14px;
cursor:pointer;
background:#7c6cff;
color:#fff;
}

/* ===== إخفاء ===== */
.hidden{display:none}

/* ===== الهيرو ===== */
#hero{
position:relative;
height:90vh;
}

#hero img{
width:100%;
height:100%;
object-fit:cover;
}

#hero::after{
content:"";
position:absolute;
top:0;left:0;
width:100%;
height:100%;
background:rgba(0,0,0,.45);
}

#heroText{
position:absolute;
bottom:30px;
width:100%;
z-index:2;
}

/* ===== الاشتراكات ===== */
#subs{
padding:40px 20px;
}

.cards{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
gap:20px;
max-width:1100px;
margin:auto;
}

.card{
background:#111;
border-radius:18px;
padding:22px;
}

.card p{color:#bfc7ff;font-size:18px}

.card a{
display:block;
padding:14px;
background:#7c6cff;
border-radius:12px;
color:#fff;
text-decoration:none;
margin-top:14px;
font-size:17px;
}

/* ===== زر حماية المستهلك ===== */
.gmail-btn{
margin:40px auto;
padding:15px 26px;
background:#1abc9c;
border:none;
border-radius:16px;
color:#fff;
font-size:18px;
text-decoration:none;
max-width:360px;
display:block;
}
</style>
</head>

<body>

<!-- ===== اختيار الجنس ===== -->
<div id="genderGate">
<img id="genderBg" src="images/hero-male.jpg">
<div id="overlay"></div>

<div id="genderBox">
<h2>اختر</h2>

<button class="gender-btn"
onmouseenter="previewGender('male')"
onclick="enterSite('male')">ذكر</button>

<button class="gender-btn"
onmouseenter="previewGender('female')"
onclick="enterSite('female')">أنثى</button>
</div>
</div>

<!-- ===== الموقع ===== -->
<div id="site" class="hidden">

<div id="hero">
<img id="heroImg">
<div id="heroText">
<h1>TIMO CLUB</h1>
<p>أهلاً بك في TIMO CLUB</p>
</div>
</div>

<section id="subs">
<div class="cards">

<div class="card">
<h3>شهر</h3>
<p>865 جنيه</p>
<a href="https://wa.me/201034381180?text=اشتراك شهر">اشترك</a>
</div>

<div class="card">
<h3>شهرين</h3>
<p>1450 جنيه</p>
<a href="https://wa.me/201034381180?text=اشتراك شهرين">اشترك</a>
</div>

<div class="card">
<h3>3 شهور</h3>
<p>2050 جنيه</p>
<a href="https://wa.me/201034381180?text=اشتراك 3 شهور">اشترك</a>
</div>

<div class="card">
<h3>5 شهور</h3>
<p>2500 جنيه</p>
<a href="https://wa.me/201034381180?text=اشتراك 5 شهور">اشترك</a>
</div>

<div class="card">
<h3>6 شهور</h3>
<p>3650 جنيه</p>
<a href="https://wa.me/201034381180?text=اشتراك 6 شهور">اشترك</a>
</div>

<div class="card">
<h3>12 شهر</h3>
<p>6895 جنيه</p>
<a href="https://wa.me/201034381180?text=اشتراك 12 شهر">اشترك</a>
</div>

</div>

<a class="gmail-btn"
href="mailto:support@timoclub.com?subject=حماية المستهلك">
حماية المستهلك
</a>

</section>
</div>

<script>
function previewGender(type){
document.getElementById("genderBg").src =
type==="male" ? "images/hero-male.jpg" : "images/hero-female.jpg";
}

function enterSite(type){
document.getElementById("genderGate").style.display="none";
document.getElementById("site").classList.remove("hidden");
document.getElementById("heroImg").src =
type==="male" ? "images/hero-male.jpg" : "images/hero-female.jpg";
}
</script>

</body>
</html>
