<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مناهج الكويت - تصفح آمن</title>
    <style>
        :root {
            --primary: #00897b;
            --secondary: #26a69a;
            --bg: #f4f7f6;
        }

        body, html {
            height: 100%;
            margin: 0;
            font-family: 'Segoe UI', sans-serif;
            background: var(--bg);
            overflow: hidden; /* لمنع السكرول المزدوج */
        }

        /* واجهة الموقع الرئيسية */
        .home-screen {
            padding: 20px;
            height: 100%;
            overflow-y: auto;
            text-align: center;
        }

        header {
            background: var(--primary);
            color: white;
            padding: 30px;
            border-radius: 15px;
            margin-bottom: 20px;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
            gap: 15px;
            max-width: 900px;
            margin: auto;
        }

        .card {
            background: white;
            padding: 20px;
            border-radius: 12px;
            cursor: pointer;
            font-weight: bold;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            transition: 0.3s;
            border: 1px solid #ddd;
        }

        .card:hover { transform: translateY(-5px); background: #e0f2f1; border-color: var(--primary); }

        /* شاشة عرض الكتاب (مخفية في البداية) */
        .viewer-screen {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: white;
            z-index: 1000;
            flex-direction: column;
        }

        /* شريط التحكم العلوي داخل العرض */
        .viewer-header {
            background: #333;
            color: white;
            padding: 10px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .back-btn {
            background: #ff5252;
            color: white;
            border: none;
            padding: 8px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            font-family: 'Segoe UI';
        }

        .back-btn:hover { background: #ff1744; }

        iframe {
            flex-grow: 1;
            width: 100%;
            border: none;
        }
    </style>
</head>
<body>

<div class="home-screen" id="homeScreen">
    <header>
        <h1>🇰🇼 مكتبة المناهج</h1>
        <p>تصفح جميع الكتب دون مغادرة الموقع</p>
    </header>

    <div class="grid">
        <div class="card" onclick="showBook('https://www.kwedufiles.com/1', 'الصف الأول')">الصف الأول</div>
        <div class="card" onclick="showBook('https://www.kwedufiles.com/6', 'الصف السادس')">الصف السادس</div>
        <div class="card" onclick="showBook('https://www.kwedufiles.com/10', 'الصف العاشر')">الصف العاشر</div>
        <div class="card" onclick="showBook('https://www.kwedufiles.com/13', 'الصف 12 علمي')">الصف 12 علمي</div>
    </div>
</div>

<div class="viewer-screen" id="viewerScreen">
    <div class="viewer-header">
        <span id="bookTitle">جاري العرض...</span>
        <button class="back-btn" onclick="closeBook()">رجوع للموقع ↩️</button>
    </div>
    <iframe id="frame"></iframe>
</div>

<script>
    function showBook(url, title) {
        document.getElementById('homeScreen').style.display = 'none';
        document.getElementById('viewerScreen').style.display = 'flex';
        document.getElementById('frame').src = url;
        document.getElementById('bookTitle').innerText = "أنت تتصفح الآن: " + title;
    }

    function closeBook() {
        document.getElementById('homeScreen').style.display = 'block';
        document.getElementById('viewerScreen').style.display = 'none';
        document.getElementById('frame').src = ""; // تفريغ الرابط لتوفير الذاكرة
    }
</script>

</body>
</html>
