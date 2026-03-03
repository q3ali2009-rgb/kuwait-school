<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>المناهج الكويتية</title>

<style>
*{
    box-sizing:border-box;
}

body{
    margin:0;
    font-family:Tahoma, Arial, sans-serif;
    background:#f2f4f8;
}

/* الهيدر */
header{
    background:#006c35;
    color:white;
    padding:20px;
    text-align:center;
    font-size:22px;
}

/* التخطيط */
.wrapper{
    display:flex;
}

/* القائمة الجانبية */
.sidebar{
    width:260px;
    background:#014421;
    color:white;
    min-height:100vh;
    padding:20px;
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

.sidebar li{
    padding:12px;
    cursor:pointer;
    border-radius:6px;
    margin-bottom:5px;
}

.sidebar li:hover{
    background:#006c35;
}

/* المحتوى */
.content{
    flex:1;
    padding:30px;
}

.card{
    background:white;
    padding:20px;
    border-radius:12px;
    box-shadow:0 4px 10px rgba(0,0,0,0.1);
    margin-bottom:20px;
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
    border-radius:6px;
    cursor:pointer;
    font-size:14px;
}

button:hover{
    background:#014421;
}
</style>
</head>

<body>

<header>
📚 موقع المناهج الكويتية - الكتب الجديدة 2025 / 2026
</header>

<div class="wrapper">

<!-- القائمة الجانبية -->
<div class="sidebar">
    <h3>القائمة الرئيسية</h3>
    <ul>
        <li onclick="showContent('primary')">المرحلة الابتدائية</li>
        <li onclick="showContent('middle')">المرحلة المتوسطة</li>
        <li onclick="showContent('secondary')">المرحلة الثانوية</li>
        <li onclick="showContent('banks')">بنوك الأسئلة</li>
        <li onclick="showContent('books')">الكتب الجديدة</li>
    </ul>
</div>

<!-- المحتوى -->
<div class="content">

<div class="welcome">
👋 أهلاً وسهلاً بك في موقع المناهج الكويتية  
نتمنى لك التوفيق والنجاح 🌟
</div>

<div id="mainContent">

<div class="card">
<h2>اختر قسم من القائمة لعرض المحتوى</h2>
<p>جميع الكتب المعروضة هي النسخ الجديدة المحدثة لعام 2025 / 2026</p>
</div>

</div>

</div>
</div>

<script>

function showContent(section){

var box = document.getElementById("mainContent");

if(section === "primary"){
box.innerHTML = `
<div class="card">
<h2>📘 المرحلة الابتدائية</h2>
<p>الصف الأول - الثاني - الثالث - الرابع - الخامس</p>
<button onclick="alert('سيتم إضافة روابط الكتب قريباً')">عرض الكتب الجديدة</button>
</div>`;
}

else if(section === "middle"){
box.innerHTML = `
<div class="card">
<h2>📗 المرحلة المتوسطة</h2>
<p>الصف السادس - السابع - الثامن - التاسع</p>
<button onclick="alert('سيتم إضافة روابط الكتب قريباً')">عرض الكتب الجديدة</button>
</div>`;
}

else if(section === "secondary"){
box.innerHTML = `
<div class="card">
<h2>📕 المرحلة الثانوية</h2>
<p>الصف العاشر - الحادي عشر - الثاني عشر</p>
<button onclick="alert('سيتم إضافة روابط الكتب قريباً')">عرض الكتب الجديدة</button>
</div>`;
}

else if(section === "banks"){
box.innerHTML = `
<div class="card">
<h2>📝 بنوك الأسئلة</h2>
<p>نماذج اختبارات + مراجعات نهائية + أسئلة محلولة</p>
<button onclick="alert('سيتم إضافة بنوك الأسئلة قريباً')">تحميل بنك الأسئلة</button>
</div>`;
}

else if(section === "books"){
box.innerHTML = `
<div class="card">
<h2>📚 الكتب التعليمية الجديدة 2025 - 2026</h2>
<p>كتب محدثة حسب المنهج الكويتي الجديد بصيغة PDF</p>
<button onclick="alert('سيتم إضافة روابط التحميل قريباً')">تحميل الكتب</button>
</div>`;
}

}

</script>

</body>
</html>
