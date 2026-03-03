<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>بوابة المناهج الكويتية</title>
    <style>
        :root {
            --primary: #00796b;
            --secondary: #26a69a;
            --dark: #004d40;
            --light: #f4f7f6;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--light);
            margin: 0;
            overflow-x: hidden;
        }

        /* القائمة الجانبية (الثلاث نقاط) */
        .sidebar {
            height: 100%;
            width: 0;
            position: fixed;
            z-index: 2000;
            top: 0;
            right: 0;
            background-color: var(--dark);
            overflow-x: hidden;
            transition: 0.5s;
            padding-top: 60px;
        }

        .sidebar a {
            padding: 15px 32px;
            text-decoration: none;
            font-size: 18px;
            color: #818181;
            display: block;
            transition: 0.3s;
        }

        .sidebar a:hover { color: #f1f1f1; }

        .sidebar .closebtn {
            position: absolute;
            top: 0;
            left: 25px;
            font-size: 36px;
            margin-left: 50px;
        }

        /* الهيدر */
        header {
            background: var(--primary);
            color: white;
            padding: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .menu-icon { font-size: 30px; cursor: pointer; }

        /* حاويات الشاشات */
        .screen {
            display: none;
            padding: 20px;
            text-align: center;
            animation: fadeIn 0.4s;
        }

        .active-screen { display: block; }

        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }

        .welcome-card {
            background: white;
            padding: 40px 20px;
            border-radius: 20px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            margin-top: 50px;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
            gap: 15px;
            max-width: 800px;
            margin: 20px auto;
        }

        .btn {
            background: white;
            padding: 20px;
            border-radius: 15px;
            border: 2px solid var(--primary);
            color: var(--dark);
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
        }

        .btn:hover { background: var(--primary); color: white; }

        .back-btn {
            background: #e74c3c;
            color: white;
            border: none;
            padding: 10px 25px;
            border-radius: 10px;
            margin-top: 20px;
            cursor: pointer;
        }

        .stage-title {
            margin-top: 30px;
            color: var(--dark);
            border-bottom: 2px solid var(--primary);
            display: inline-block;
            padding-bottom: 5px;
        }

        iframe {
            width: 100%;
            height: 80vh;
            border: none;
            margin-top: 10px;
        }
    </style>
</head>
<body>

<div id="mySidebar" class="sidebar">
    <a href="javascript:void(0)" class="closebtn" onclick="closeNav()">×</a>
    <a href="#" onclick="showScreen('home')">الرئيسية</a>
    <a href="#" onclick="showScreen('grades')">المراحل الدراسية</a>
    <a href="https://moe.edu.kw" target="_blank">موقع الوزارة</a>
</div>

<header>
    <div></div> <h2>بوابة المناهج</h2>
    <span class="menu-icon" onclick="openNav()">&#9776;</span>
</header>

<div id="home" class="screen active-screen">
    <div class="welcome-card">
        <h1>حياكم الله في موقعكم التعليمي 🇰🇼</h1>
        <p>كل ما يحتاجه الطالب الكويتي في مكان واحد</p>
        <button class="btn" style="background:var(--primary); color:white; width:200px;" onclick="showScreen('grades')">ابدأ التصفح</button>
    </div>
</div>

<div id="grades" class="screen">
    <h3 class="stage-title">المرحلة الابتدائية</h3>
    <div class="grid">
        <button class="btn" onclick="showSemester('الصف الأول')">الأول</button>
        <button class="btn" onclick="showSemester('الصف الثاني')">الثاني</button>
        <button class="btn" onclick="showSemester('الصف الثالث')">الثالث</button>
        <button class="btn" onclick="showSemester('الصف الرابع')">الرابع</button>
        <button class="btn" onclick="showSemester('الصف الخامس')">الخامس</button>
    </div>

    <h3 class="stage-title">المرحلة المتوسطة</h3>
    <div class="grid">
        <button class="btn" onclick="showSemester('الصف السادس')">السادس</button>
        <button class="btn" onclick="showSemester('الصف السابع')">السابع</button>
        <button class="btn" onclick="showSemester('الصف الثامن')">الثامن</button>
        <button class="btn" onclick="showSemester('الصف التاسع')">التاسع</button>
    </div>

    <h3 class="stage-title">المرحلة الثانوية</h3>
    <div class="grid">
        <button class="btn" onclick="showSemester('الصف العاشر')">العاشر</button>
        <button class="btn" onclick="showSemester('الصف 11')">11 (علمي/أدبي)</button>
        <button class="btn" onclick="showSemester('الصف 12')">12 (علمي/أدبي)</button>
    </div>
    <button class="back-btn" onclick="showScreen('home')">رجوع</button>
</div>

<div id="semesters" class="screen">
    <h2 id="selectedGrade"></h2>
    <div class="grid">
        <button class="btn" onclick="viewContent('الفصل الأول')">الفصل الدراسي الأول</button>
        <button class="btn" onclick="viewContent('الفصل الثاني')">الفصل الدراسي الثاني</button>
    </div>
    <button class="back-btn" onclick="showScreen('grades')">رجوع لاختيار الصف</button>
</div>

<div id="viewer" class="screen">
    <h3 id="viewingTitle"></h3>
    <iframe id="contentFrame" src=""></iframe>
    <br>
    <button class="back-btn" onclick="showScreen('semesters')">رجوع لاختيار الفصل</button>
</div>

<script>
    let currentGrade = "";

    function openNav() { document.getElementById("mySidebar").style.width = "250px"; }
    function closeNav() { document.getElementById("mySidebar").style.width = "0"; }

    function showScreen(screenId) {
        // إخفاء جميع الشاشات
        document.querySelectorAll('.screen').forEach(s => s.classList.remove('active-screen'));
        // إظهار الشاشة المطلوبة
        document.getElementById(screenId).classList.add('active-screen');
        closeNav();
    }

    function showSemester(gradeName) {
        currentGrade = gradeName;
        document.getElementById('selectedGrade').innerText = "اختر الفصل الدراسي لـ " + gradeName;
        showScreen('semesters');
    }

    function viewContent(semester) {
        document.getElementById('viewingTitle').innerText = currentGrade + " - " + semester;
        // هنا تضعين الروابط الفعلية مستقبلاً
        document.getElementById('contentFrame').src = "https://moe.edu.kw"; 
        showScreen('viewer');
    }
</script>

</body>
</html>
