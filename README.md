<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>بوابة مناهج الكويت الشاملة</title>
    <style>
        :root {
            --primary: #00796b;
            --secondary: #004d40;
            --bg: #f0f4f4;
            --text: #333;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            margin: 0;
            padding: 10px;
            color: var(--text);
        }

        .container {
            max-width: 900px;
            margin: auto;
        }

        header {
            text-align: center;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 30px 15px;
            border-radius: 20px;
            margin-bottom: 25px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        h1 { margin: 0; font-size: 1.8rem; }
        header p { margin: 10px 0 0; opacity: 0.9; }

        .stage-title {
            background: var(--secondary);
            color: white;
            padding: 10px 20px;
            border-radius: 10px;
            margin: 25px 0 15px;
            display: inline-block;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
            gap: 15px;
        }

        .card {
            background: white;
            padding: 20px 10px;
            border-radius: 15px;
            text-align: center;
            text-decoration: none;
            color: var(--text);
            font-weight: bold;
            transition: 0.3s;
            border-bottom: 4px solid #ddd;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .card:hover {
            transform: translateY(-5px);
            border-bottom-color: var(--primary);
            background: #e0f2f1;
        }

        .card i { font-size: 1.2rem; color: var(--primary); }

        footer {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            font-size: 0.8rem;
            color: #666;
        }

        /* تحسين للموبايل */
        @media (max-width: 480px) {
            .grid { grid-template-columns: repeat(2, 1fr); }
            h1 { font-size: 1.4rem; }
        }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>🇰🇼 مكتبة مناهج الكويت 🇰🇼</h1>
        <p>تحميل مباشر لجميع الكتب المدرسية (PDF)</p>
    </header>

    <div class="stage-title">المرحلة الابتدائية</div>
    <div class="grid">
        <a href="https://www.kwedufiles.com/1" target="_blank" class="card">الصف الأول</a>
        <a href="https://www.kwedufiles.com/2" target="_blank" class="card">الصف الثاني</a>
        <a href="https://www.kwedufiles.com/3" target="_blank" class="card">الصف الثالث</a>
        <a href="https://www.kwedufiles.com/4" target="_blank" class="card">الصف الرابع</a>
        <a href="https://www.kwedufiles.com/5" target="_blank" class="card">الصف الخامس</a>
    </div>

    <div class="stage-title">المرحلة المتوسطة</div>
    <div class="grid">
        <a href="https://www.kwedufiles.com/6" target="_blank" class="card">الصف السادس</a>
        <a href="https://www.kwedufiles.com/7" target="_blank" class="card">الصف السابع</a>
        <a href="https://www.kwedufiles.com/8" target="_blank" class="card">الصف الثامن</a>
        <a href="https://www.kwedufiles.com/9" target="_blank" class="card">الصف التاسع</a>
    </div>

    <div class="stage-title">المرحلة الثانوية</div>
    <div class="grid">
        <a href="https://www.kwedufiles.com/10" target="_blank" class="card">الصف العاشر</a>
        <a href="https://www.kwedufiles.com/11" target="_blank" class="card">الصف 11 (علمي)</a>
        <a href="https://www.kwedufiles.com/12" target="_blank" class="card">الصف 11 (أدبي)</a>
        <a href="https://www.kwedufiles.com/13" target="_blank" class="card">الصف 12 (علمي)</a>
        <a href="https://www.kwedufiles.com/14" target="_blank" class="card">الصف 12 (أدبي)</a>
    </div>

    <footer>
        <p>جميع الحقوق محفوظة - تم البرمجة لخدمة طلاب الكويت 2026</p>
    </footer>
</div>

</body>
</html>
