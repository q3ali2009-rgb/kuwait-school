حياكمم
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>بوابة المناهج الكويتية</title>
    <style>
        :root { --primary: #00796b; --dark: #004d40; --bg: #f4f7f6; }
        body { font-family: 'Segoe UI', sans-serif; margin: 0; background: var(--bg); display: flex; flex-direction: column; min-height: 100vh; }
        
        /* الهيدر والقائمة الجانبية */
        header { background: var(--primary); color: white; padding: 15px; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 0; z-index: 1000; }
        .sidebar { height: 100%; width: 0; position: fixed; z-index: 2000; top: 0; right: 0; background: var(--dark); overflow-x: hidden; transition: 0.5s; padding-top: 60px; }
        .sidebar a { padding: 15px 25px; text-decoration: none; color: #ccc; display: block; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .sidebar a:hover { background: var(--primary); color: white; }

        /* الشاشات */
        .screen { display: none; padding: 20px; text-align: center; }
        .active-screen { display: block; }
        
        .welcome-card { background: white; padding: 40px; border-radius: 20px; box-shadow: 0 4px 15px rgba(0,0,0,0.05); margin-top: 20px; }
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(130px, 1fr)); gap: 15px; max-width: 800px; margin: 20px auto; }
        
        .btn { background: white; padding: 15px; border-radius: 12px; border: 2px solid var(--primary); font-weight: bold; cursor: pointer; transition: 0.3s; }
        .btn:hover { background: var(--primary); color: white; }
        .btn-gold { background: #ffc107; border-color: #ffa000; }

        /* شاشة العرض الكاملة (للبقاء في الموقع) */
        #viewer { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: white; z-index: 3000; display: none; flex-direction: column; }
        .viewer-bar { background: #333; color: white; padding: 10px 20px; display: flex; justify-content: space-between; align-items: center; }
        iframe { width: 100%; flex-grow: 1; border: none; }
        
        .back-btn { background: #e74c3c; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer; font-weight: bold; }
        footer { background: #222; color: #999; text-align: center; padding: 15px; margin-top: auto; }
    </style>
</head>
<body>

<div id="mySidebar" class="sidebar">
    <a href="javascript:void(0)" style="font-size:30px" onclick="closeNav()">×</a>
    <a href="#" onclick="showScreen('home')">🏠 الرئيسية</a>
    <a href="#" onclick="showScreen('grades')">📚 المناهج الدراسية</a>
    <a href="#" onclick="openExternal('https://www.kwedufiles.com/qbank', 'بنوك الأسئلة المحلولة')">📝 بنوك الأسئلة</a>
    <a href="https://moe.edu.kw" target="_blank">🔗 موقع الوزارة</a>
</div>

<header>
    <div style="width:40px"></div>
    <h3>بوابة المناهج الكويتية</h3>
    <span style="font-size:30px;cursor:pointer" onclick="openNav()">&#9776;</span>
</header>

<div id="home" class="screen active-screen">
    <div class="welcome-card">
        <h1>حياكم الله بموقعكم 🇰🇼</h1>
        <p>كل المناهج وبنوك الأسئلة بمكان واحد</p>
        <button class="btn" style="background:var(--primary); color:white; width:200px" onclick="showScreen('grades')">دخول المكتبة</button>
    </div>
</div>

<div id="grades" class="screen">
    <h3 style="text-align:right">اختر المرحلة الدراسية:</h3>
    <div class="grid">
        <button class="btn" onclick="showSemester('الأول', '1')">1</button>
        <button class="btn" onclick="showSemester('الثاني', '2')">2</button>
        <button class="btn" onclick="showSemester('الثالث', '3')">3</button>
        <button class="btn" onclick="showSemester('الرابع', '4')">4</button>
        <button class="btn" onclick="showSemester('الخامس', '5')">5</button>
        <button class="btn" onclick="showSemester('السادس', '6')">6</button>
        <button class="btn" onclick="showSemester('السابع', '7')">7</button>
        <button class="btn" onclick="showSemester('الثامن', '8')">8</button>
        <button class="btn" onclick="showSemester('التاسع', '9')">9</button>
        <button class="btn" onclick="showSemester('العاشر', '10')">10</button>
        <button class="btn" onclick="showSemester('11', '11')">11</button>
        <button class="btn" onclick="showSemester('12', '12')">12</button>
    </div>
    <div class="grid">
        <button class="btn btn-gold" onclick="openExternal('https://www.kwedufiles.com/qbank', 'بنوك الأسئلة المحلولة')">📝 بنوك الأسئلة المحلولة</button>
    </div>
</div>

<div id="semesters" class="screen">
    <h2 id="gradeTitle"></h2>
    <div class="grid">
        <button class="btn" onclick="openBook('1')">الفصل الأول</button>
        <button class="btn" onclick="openBook('2')">الفصل الثاني</button>
    </div>
    <button class="back-btn" onclick="showScreen('grades')">رجوع</button>
</div>

<div id="viewer">
    <div class="viewer-bar">
        <span id="viewTitle">جاري التحميل...</span>
        <button class="back-btn" onclick="closeViewer()">❌ إغلاق والرجوع لموقعي</button>
    </div>
    <iframe id="mainFrame" src=""></iframe>
</div>

<footer>
    <p>جميع الحقوق محفوظة &copy; 2026 - بوابة المناهج الكويتية</p>
</footer>

<script>
    let selID = "";
    let selName = "";

    function openNav() { document.getElementById("mySidebar").style.width = "250px"; }
    function closeNav() { document.getElementById("mySidebar").style.width = "0"; }

    function showScreen(id) {
        document.querySelectorAll('.screen').forEach(s => s.classList.remove('active-screen'));
        document.getElementById(id).classList.add('active-screen');
        closeNav();
    }

    function showSemester(name, id) {
        selID = id; selName = name;
        document.getElementById('gradeTitle').innerText = "منهج الصف " + name;
        showScreen('semesters');
    }

    function openBook(sem) {
        let url = "https://www.kwedufiles.com/" + selID;
        openExternal(url, "منهج " + selName + " - الفصل " + sem);
    }

    function openExternal(url, title) {
        document.getElementById('viewTitle').innerText = title;
        document.getElementById('mainFrame').src = url;
        document.getElementById('viewer').style.display = "flex";
        closeNav();
    }

    function closeViewer() {
        document.getElementById('viewer').style.display = "none";
        document.getElementById('mainFrame').src = "";
    }
</script>

</body>
</html>
