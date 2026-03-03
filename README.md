<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>المناهج الكويتية</title>

<style>
body{
    margin:0;
    font-family: 'Tahoma', sans-serif;
    background:#f4f6f9;
}

header{
    background:#006c35;
    color:white;
    padding:20px;
    text-align:center;
    font-size:22px;
}

.container{
    display:flex;
}

/* القائمة الجانبية */
.sidebar{
    width:250px;
    background:#014421;
    min-height:100vh;
    padding:20px;
    color:white;
}

.sidebar h3{
    margin-top:0;
    border-bottom:1px solid #fff;
    padding-bottom:10px;
}

.sidebar ul{
    list-style:none;
    padding:0;
}

.sidebar ul li{
    padding:10px 0;
    cursor:pointer;
}

.sidebar ul li:hover{
    background:#006c35;
    padding-right:10px;
}

/* المحتوى */
.content{
    flex:1;
    padding:30px;
}

.card{
    background:white;
    padding:20px;
    margin-bottom:20px;
    border-radius:10px;
    box-shadow:0 4px 10px rgba(0,0,0,0.1);
}

.welcome{
    font-size:20px;
    color:#006c35;
    margin-bottom:20px;
}

button{
    background:#006c35;
    color:white;
    border:none;
    padding:10px 15px;
    border-radius:5px;
    cursor:pointer;
}

button:hover{
    background:#014421;
}
</style>
</head>

<body>

<header>
📚 موقع المناهج الكويتية - الكتب الجديدة 2025/2026
</header>

<div class="container">

<!-- القائمة -->
<div class="sidebar">
    <h3>القائمة الرئيسية</h3>
    <ul>
        <li onclick="showSection('primary')">المرحلة الابتدائية</li>
        <li onclick="showSection('middle')">المرحلة المتوسطة</li>
        <li onclick="showSection('secondary')">المرحلة الثانوية</li>
        <li onclick="showSection('banks')">بنوك الأسئلة</li>
        <li onclick="showSection('books')">الكتب الجديدة</li>
    </ul>
</div>

<!-- المحتوى -->
<div class="content">

<div class="welcome">
👋 أهلاً وسهلاً بك في موقع المناهج الكويتية الرسمي غير التابع للوزارة  
نتمنى لك التوفيق والنجاح 🌟
</div>

<div id="sectionContent">

<div class="card">
<h2>اختر من القائمة لعرض المحتوى</h2>
<p>جميع الكتب المعروضة هي النسخ الجديدة المحدثة للعام الدراسي 2025 / 2026</p>
</div>

</div>

</div>
</div>

<script>

function showSection(section){

let content = document.getElementById("sectionContent");

if(section === "primary"){
content.innerHTML = `
<div class="card">
<h2>📘 المرحلة الابتدائية</h2>
<p>الصف الأول - الثاني - الثالث - الرابع - الخامس</p>
<button>عرض الكتب الجديدة</button>
</div>`;
}

if(section === "middle"){
content.innerHTML = `
<div class="card">
<h2>📗 المرحلة المتوسطة</h2>
<p>الصف السادس - السابع - الثامن - التاسع</p>
<button>عرض الكتب الجديدة</button>
</div>`;
}

if(section === "secondary"){
content.innerHTML = `
<div class="card">
<h2>📕 المرحلة الثانوية</h2>
<p>الصف العاشر - الحادي عشر - الثاني عشر</p>
<button>عرض الكتب الجديدة</button>
</div>`;
}

if(section === "banks"){
content.innerHTML = `
<div class="card">
<h2>📝 بنوك الأسئلة</h2>
<p>نماذج اختبارات + مراجعات نهائية + أسئلة محلولة</p>
<button>تحميل بنك الأسئلة</button>
</div>`;
}

if(section === "books"){
content.innerHTML = `
<div class="card">
<h2>📚 الكتب التعليمية الجديدة 2025-2026</h2>
<p>جميع الكتب بصيغة PDF ومحدثة حسب المنهج الكويتي الجديد</p>
<button>تحميل الكتب</button>
</div>`;
}

}

</script>

</body>
</html>
