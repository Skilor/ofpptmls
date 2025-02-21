<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>liens de site Web</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            line-height: 1.6;
            background-color: #f4f4f9; /* خلفية ثابتة بلون فاتح */
            position: relative;
        }

        /* عرض الساعة والتاريخ في الأعلى */
        .header {
            display: flex;
            flex-direction: column;
            align-items: center; /* تمركز النصوص أفقيًا */
            padding: 10px 20px;
            color: black; /* لون النص أسود */
        }

        .clock, .date {
            font-size: 24px; /* زيادة حجم الخط */
            font-weight: bold;
            margin: 5px 0; /* إضافة مسافة بين الساعة والتاريخ */
        }

        /* نص GÉNIE ÉLECTRIQUE باللون الأزرق */
        .footer-text {
            position: absolute;
            bottom: 10px;
            left: 10px;
            font-size: 14px;
            color: #1C45E4; /* لون أزرق داكن */
            font-weight: bold;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
        }

        /* تصميم container */
        .container {
            max-width: 600px;
            margin: 20px auto 0;
            background: rgba(255, 255, 255, 0.9); /* خلفية شبه شفافة */
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }

        h1 {
            text-align: center;
            color: #333333;
        }

        .link-item {
            margin-bottom: 20px;
            text-align: center;
        }

        .link-item a {
            display: inline-block;
            padding: 10px 20px;
            color: #ffffff;
            text-decoration: none;
            border-radius: 5px;
            transition: transform 0.3s ease;
        }

        .link-item a:hover {
            transform: scale(1.1);
        }

        .myway {
            background-color: #16CDE3;
        }

        .ofppt-langue {
            background-color: #8D9492;
        }

        .scholarvox {
            background-color: #1D9D17;
        }

        .ofppt {
            background-color: #1C45E4;
        }
    </style>
</head>
<body>
    <!-- عرض الساعة والتاريخ في الأعلى -->
    <div class="header">
        <div id="clock" class="clock"></div>
        <div id="date" class="date"></div>
    </div>

    <div class="container">
        <h1>liens de site Web</h1>
        <div class="link-item">
            <a href="https://www.myway.ac.ma/fr" target="_blank" class="myway">MY WAY</a>
        </div>
        <div class="link-item">
            <a href="https://altissia.org/fr/ofppt-langues" target="_blank" class="ofppt-langue">OFPPT LANGUE</a>
        </div>
        <div class="link-item">
            <a href="https://www.scholarvox.com/" target="_blank" class="scholarvox">SCHOLARVOX</a>
        </div>
        <div class="link-item">
            <a href="https://www.ofppt.ma/" target="_blank" class="ofppt">OFPPT</a>
        </div>
    </div>

    <!-- النص في الأسفل على اليسار -->
    <div class="footer-text">GÉNIE ÉLECTRIQUE 103</div>

    <script>
        // وظيفة لإظهار الوقت والتاريخ
        function updateDateTime() {
            const now = new Date();
            const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
            document.getElementById('clock').textContent = now.toLocaleTimeString();
            document.getElementById('date').textContent = now.toLocaleDateString('fr-FR', options);
        }

        // تحديث الوقت والتاريخ كل ثانية
        setInterval(updateDateTime, 1000);

        // بدء العرض عند تحميل الصفحة
        updateDateTime();
    </script>
</body>
</html>
