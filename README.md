# kuwait-school
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مناهج الكويت التعليمية</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --accent-color: #3498db;
            --bg-color: #f4f7f6;
            --white: #ffffff;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            margin: 0;
            padding: 20px;
            color: var(--primary-color);
        }

        header {
            text-align: center;
            padding: 40px 0;
            background: var(--primary-color);
            color: var(--white);
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
        }

        .stage-section {
            margin-bottom: 40px;
        }

        .stage-title {
            border-right: 5px solid var(--accent-color);
            padding-right: 15px;
            margin-bottom: 20px;
            font-size: 1.5rem;
            color: var(--primary-color);
        }

        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 15px;
        }

        .grade-card {
            background: var(--white);
            padding: 20px;
            text-align: center;
            border-radius: 12px;
            text-decoration: none;
            color: var(--primary-color);
            font-weight: bold;
            transition: all 0.3s ease;
            border: 1px solid #eee;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
        }

        .grade-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
            border-color: var(--accent-color);
            color: var(--accent-color);
        }

        .grade-card i {
            font-size: 24px;
        }

        footer {
            text-align: center;
            margin-top: 50px;
            font-size: 0.9rem;
            color: #7f8c8d;
        }

        /* لمسات جمالية للموبايل */
        @media (max-width: 600px) {
            .grid-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>مكتبة مناهج الكويت الرقمية</h1>
        <p>جميع الكتب المدرسية من الصف الأول إلى الثاني عشر</p>
    </header>

    <div class="stage-section">
        <h2 class="stage-title">المرحلة الابتدائية</h2>
        <div class="grid-container">
            <a href="#" class="grade-card"><span>الصف الأول</span></a>
            <a href="#" class="grade-card"><span>الصف الثاني</span></a>
            <a href="#" class="grade-card"><span>الصف الثالث</span></a>
            <a href="#" class="grade-card"><span>الصف الرابع</span></a>
            <a href="#" class="grade-card"><span>الصف الخامس</span></a>
        </div>
    </div>

    <div class="stage-section">
        <h2 class="stage-title">المرحلة المتوسطة</h2>
        <div class="grid-container">
            <a href="#" class="grade-card"><span>الصف السادس</span></a>
            <a href="#" class="grade-card"><span>الصف السابع</span></a>
            <a href="#" class="grade-card"><span>الصف الثامن</span></a>
            <a href="#" class="grade-card"><span>الصف التاسع</span></a>
        </div>
    </div>

    <div class="stage-section">
        <h2 class="stage-title">المرحلة الثانوية</h2>
        <div class="grid-container">
            <a href="#" class="grade-card"><span>الصف العاشر</span></a>
            <a href="#" class="grade-card"><span>الصف الحادي عشر</span></a>
            <a href="#" class="grade-card"><span>الصف الثاني عشر</span></a>
        </div>
    </div>

    <footer>
        <p>تم تطوير الموقع لخدمة الطلبة في دولة الكويت &copy; 2026</p>
    </footer>
</div>

</body>
</html>
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مناهج الكويت الرقمية</title>
    <style>
        :root { --primary: #2c3e50; --accent: #3498db; --bg: #f4f7f6; --white: #ffffff; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background-color: var(--bg); margin: 0; padding: 20px; color: var(--primary); }
        .container { max-width: 1000px; margin: 0 auto; }
        header { text-align: center; padding: 30px; background: var(--primary); color: var(--white); border-radius: 15px; margin-bottom: 30px; }
        .stage-section { margin-bottom: 40px; }
        .stage-title { border-right: 5px solid var(--accent); padding-right: 15px; margin-bottom: 20px; font-size: 1.5rem; }
        .grid-container { display: grid; grid-template-columns: repeat(auto-fill, minmax(180px, 1fr)); gap: 15px; }
        .grade-card { background: var(--white); padding: 15px; text-align: center; border-radius: 12px; text-decoration: none; color: var(--primary); font-weight: bold; transition: 0.3s; border: 1px solid #eee; display: flex; flex-direction: column; }
        .grade-card:hover { transform: translateY(-5px); box-shadow: 0 5px 15px rgba(0,0,0,0.1); border-color: var(--accent); }
        .download-link { font-size: 0.8rem; color: #3498db; margin-top: 10px; text-decoration: underline; }
        footer { text-align: center; padding: 20px; color: #7f8c8d; }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>مكتبة المناهج الكويتية 🇰🇼</h1>
        <p>روابط مباشرة لتحميل الكتب المدرسية PDF</p>
    </header>

    <div class="stage-section">
        <h2 class="stage-title">المرحلة الثانوية</h2>
        <div class="grid-container">
            <a href="https://moe.edu.kw/student/E-book/Pages/secondary.aspx" target="_blank" class="grade-card">
                <span>الصف الثاني عشر</span>
                <span class="download-link">تحميل الكتب (علمي/أدبي)</span>
            </a>
            <a href="https://moe.edu.kw/student/E-book/Pages/secondary.aspx" target="_blank" class="grade-card">
                <span>الصف الحادي عشر</span>
                <span class="download-link">تحميل الكتب (علمي/أدبي)</span>
            </a>
            <a href="https://moe.edu.kw/student/E-book/Pages/secondary.aspx" target="_blank" class="grade-card">
                <span>الصف العاشر</span>
                <span class="download-link">تحميل جميع الكتب</span>
            </a>
        </div>
    </div>

    <div class="stage-section">
        <h2 class="stage-title">المرحلة المتوسطة</h2>
        <div class="grid-container">
            <a href="https://moe.edu.kw/student/E-book/Pages/intermediate.aspx" target="_blank" class="grade-card">
                <span>الصف التاسع</span>
                <span class="download-link">رابط الكتب الرسمي</span>
            </a>
            <a href="https://moe.edu.kw/student/E-book/Pages/intermediate.aspx" target="_blank" class="grade-card">
                <span>الصف الثامن</span>
                <span class="download-link">رابط الكتب الرسمي</span>
            </a>
            <a href="https://moe.edu.kw/student/E-book/Pages/intermediate.aspx" target="_blank" class="grade-card">
                <span>الصف السابع</span>
                <span class="download-link">رابط الكتب الرسمي</span>
            </a>
            <a href="https://moe.edu.kw/student/E-book/Pages/intermediate.aspx" target="_blank" class="grade-card">
                <span>الصف السادس</span>
                <span class="download-link">رابط الكتب الرسمي</span>
            </a>
        </div>
    </div>

    <div class="stage-section">
        <h2 class="stage-title">المرحلة الابتدائية</h2>
        <div class="grid-container">
            <a href="https://moe.edu.kw/student/E-book/Pages/primary.aspx" target="_blank" class="grade-card">
                <span>الصفوف 1 - 5</span>
                <span class="download-link">تحميل كتب الابتدائي</span>
            </a>
        </div>
    </div>

    <footer>
        <p>حقوق المناهج محفوظة لوزارة التربية - دولة الكويت</p>
    </footer>
</div>

</body>
</html>
