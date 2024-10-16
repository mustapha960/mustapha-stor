<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>متجر الملابس والإكسسوارات والكتب</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }

        /* الهيدر مع خلفية صورة */
        header {
            color: #fff;
            padding: 20px;
            background-image: url('c:\Users\HP FOLIO 9470m\Desktop\WhatsApp Image 2024-10-16 at 12.54.16_e40ac34b.jpg'); /* استبدل بمسار الصورة التي تريدها */
            background-size: cover;
            background-position: center;
        }

        header img {
            width: 100px;
            height: auto;
        }

        h1 {
            margin: 10px 0;
            font-size: 32px;
        }

        /* تنسيق التنقل */
        nav {
            margin: 20px 0;
        }

        nav button {
            margin: 10px;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            background-color: #333;
            color: white;
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }

        nav button:hover {
            background-color: #555;
        }

        /* محتوى الصفحة */
        section {
            margin-top: 20px;
            padding: 20px;
            background-color: #fff;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        /* تنسيق المنتجات */
        .product {
            margin-bottom: 20px;
        }

        .product img {
            width: 200px;
            height: auto;
            margin-bottom: 10px;
            border-radius: 5px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .product h3 {
            margin: 0;
            font-size: 20px;
        }

        .product p {
            margin: 5px 0;
        }

        .product .price {
            font-weight: bold;
            color: #e60000;
        }

        /* جعل التنسيق متجاوب على الشاشات الصغيرة */
        @media (max-width: 768px) {
            nav button {
                width: 100%;
                margin: 5px 0;
            }

            .product img {
                width: 100%;
            }
        }
    </style>
</head>
<body>

<header>
    <img src="images/logo.png" alt="شعار المتجر"> <!-- تأكد من مسار الصورة هنا -->
    <h1>MUSTAPHA STOR</h1>
</header>

<nav>
    <button onclick="loadSection('clothes')">الملابس</button>
    <button onclick="loadSection('accessories')">الإكسسوارات</button>
    <button onclick="loadSection('books')">الكتب</button>
</nav>

<section id="content">
    <h2>مرحبًا بكم في متجرنا!</h2>
    <p>يرجى اختيار قسم لعرض المنتجات.</p>
</section>

<script>
    function loadSection(section) {
        let content = document.getElementById('content');
        let products = '';
        
        if (section === 'clothes') {
            products = `
                <div class="product">
                    <img src="images/clothes1.jpg" alt="منتج 1">
                    <h3>قميص عصري</h3>
                    <p class="price">200 جنيه</p>
                    <p>قميص عصري مناسب لجميع المناسبات.</p>
                </div>
                <div class="product">
                    <img src="images/clothes2.jpg" alt="منتج 2">
                    <h3>بنطلون جينز</h3>
                    <p class="price">300 جنيه</p>
                    <p>بنطلون جينز عالي الجودة مريح وأنيق.</p>
                </div>
            `;
        } else if (section === 'accessories') {
            products = `
                <div class="product">
                    <h3>ساعة يد</h3>
                    <p class="price">500 جنيه</p>
                    <p>ساعة يد أنيقة وعصرية تناسب جميع الأذواق.</p>
                </div>
                <div class="product">
                    <img src="images/accessory2.jpg" alt="منتج 2">
                    <h3>حقيبة يد</h3>
                    <p class="price">400 جنيه</p>
                    <p>حقيبة يد فاخرة مصنوعة من الجلد الطبيعي.</p>
                </div>
            `;
        } else if (section === 'books') {
            products = `
                <div class="product">
                    <img src="images/book1.jpg" alt="منتج 1">
                    <h3>كتاب تطوير الذات</h3>
                    <p class="price">150 جنيه</p>
                    <p>كتاب شامل حول كيفية تحقيق النجاح في الحياة.</p>
                </div>
                <div class="product">
                    <img src="images/book2.jpg" alt="منتج 2">
                    <h3>رواية مشوقة</h3>
                    <p class="price">100 جنيه</p>
                    <p>رواية تحملك إلى عالم من المغامرة والإثارة.</p>
                </div>
            `;
        }
        
        content.innerHTML = products;
    }
</script>

</body>
</html>
