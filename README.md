# Webpack Course Resources

Tehran Institute of Technology

نحوه ایجاد چهار چوب برای محتوای وب سایت :

نحوه ساخت container وب سایت :

برای اینکار کل محتوای سایت که نیاز است در ویسط صفحه قرار بگیرد را داخل یک div قرار میدهیم

اندازه ارتفاع این div مهم نیست

اما اندازه عرض آن برای ما مهم است این اندازه بر اساس اندازه دستگاه کاربر مشخص میشود

برای این کار باید وب سایت را responsive کنیم

وب سایت responsive عنی وب سایتی که به اندازه صفحه نمایش واکنش نشان میدهد

برای ساخت وب سایت responsie باید به هر آیتم چندین کد css اعمال کنیم

در css با media query ها میتوان کد را برای اندازه صفحه خاص اجرا کرد

```css
@media only screen and (min-width:768px){

کد سی اس اس

}
```
کد سی اس اس بالا در صفحات 768 به بالا اجرا میشود
```css
@media only screen and (max-width:768px){

کد سی اس اس

}
```
کد سی اس اس بالا در صفحات 768 به پایین اجرا میشود
```css
@media only screen and (min-width:768px) and (max-width:1170px){

کد سی اس اس

}
```
صفحات بین 768 الی 1170
```css
<!DOCTYPE html>

<html lang="en">

<head>

    <style>

        *{

            margin: 0;

        }

        #container {

            background-color: gray;

            margin-right: auto;

            margin-left: auto;

            height: 600px;

            width: 100%;

        }

        @media only screen and (min-width:480px) {

            #container {

                background-color: purple;

            }

        }

        @media only screen and (min-width:768px) {

            #container {

                background-color: blue;

            }

        }

        @media only screen and (min-width:960px) {

            #container {

                background-color: green;

                width: 80%;

            }

        }

        @media only screen and (min-width:1200px) {

            #container {

                background-color: red;

                width:1170px;

            }

        }

        @media only screen and (min-width:1400px) {

            #container {

                background-color: pink;

                width:1200px;

            }

        }

        @media only screen and (max-width:480px) {

            #container {

                background-color: orange;

            }

        }

    </style>

</head>

<body>

    <div id="container">

        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. A minima voluptas quibusdam, quaerat asperiores, cum illum vero pariatur excepturi accusamus ipsum odit facilis deleniti consectetur eveniet optio commodi? Molestias, ullam!</p>

    </div>

</body>

</html>
```
چیشن آیتم ها در css

دستور float  در  css : با استفاده از این دستور میتوانیم ایتم ها به سمت راست یا چپ بصورت افقی بچینیم
```css
Float:left;

Float:right;

Float:none;
```

دستور float باعث میشود آیتم ها از layout تگ پدر خارج شوند

راه حل : تنظیم ارتفاع ثابت برای تگ پدر

راه حل 2 : یک div خالی بعد آیتم های دارای float میسازیم و به آن دستور clear:right; یا clear:left; یا  clear:both; برای زمانی که هر دو float وجود دارند

این دستور مشکل float را حل میکند

ایجاد عنوان در وب سایت

برای ساخت عنوان از تگ های html زیر استفاده میکنیم
```html
<h1></h1>

....

<h6></h6>
```
تفاوت عناوین :

تفاوت اول : سایز : هر چه عدد تگ کوچکتر باشد سایز عنوان بزرگ تر است (با دستور font-size میتوان سایز انهارا عوض کرد)

تفاوت دوم : اهمیت عنوان : هر چه عدد کوچکتر باشد عنوان مهمتر است

اهمیت از نظر SEO است (مخفف Search engine optimize به فارسی بهینه سازی سایت برای موتور جستجو)

انتخاب تگ html بر اساس تگ parent در CSS
```css
Parent > child {

//css

}
```
این انتخاب میتواند تا بی نهایت ادامه ئیدا کند :
```css
 Parent > parent > parent > child {

}
```

تایپوگرافی متن در css و html

تغییر رنگ نوشته :
```css
Color:red;
```
تغییر سایز فونت نوشته :
```css
Font-size:22px;
```
نوشته بولد (ضخامت نوشته)

 1 . <b>  Text  </b>

2\. <strong> Text </strong>

هر دو نوشته را بولد میکنند و در ظاهر هیچ تفاوتی ندارند

منتها تگ strong اهمیت نوشته را از نظر seo افزایش میدهد
```css
3\. font-weight:100;

100

200

300 -> lighter

400 -> normal

500

600

700 -> bold

800

900 => bolder
```
دسته بندی تگ های HTML :

دسته تگ های

 Block level مثال : P , DIV

پیشفرض کل عرض صفحه را میپوشانند (یعنی width:100% دارند)

Width , height میگیرند

زیر هم قرار میگیرند بصورت پیشفرض (حتی اگر اندازه انهارا کوچک کنیم)

 Inline level مثال : B , Strong , span

پیشفرض به اندازه محتوای داخلشان عرض میگیرند

Width , height نمی گیرند

کنار هم قرار میگیرند

Inline block مثال : img

پیشفرض به اندازه محتوای داخلشان عرض میگیرند

Width , height میگیرند

کنار هم قرار میگیرند

برای انتخاب یک کلمه در وسط نوشته از تگ span استفاده میکنیم 

گروه inline level , container

نوشته italic :
```html
<i> Text </i>

<em> Text </em>
```

هر دو نوشته را italic  میکنند و در ظاهر هیچ تفاوتی ندارند

منتها تگ em  اهمیت نوشته را از نظر seo افزایش میدهد

هر دو تگ container , inline level

3 . Font-style:italic;

دستور css برای نوشته italic

خطوط نوشته 

Text-decoration:underline;

1.Underline

<ins> Text </ins>

زیر خط 

2.Overline

خط در بالای نوشته

Line-through3.

<del> </del> Text

روی نوشته

اگر seo مهم است از تگ html استفاده میشود

چینش متن در صفحه

دستور css

Text-align:center;

Left;

Right;

Justify تراز کردن متن

ایجاد enter در نوشته با تگ html

<br>

 این تگ empty هست

نکته مهم : در بین چند آیتم که افقی کنار هم هستند

باید آیتمی را در html اول نوشت که float دارد

ایجاد سایه برای نوشته :

دستور css : text-shadow

Text-shadow:0px 0px 0px color;

عدد اول : موقعیت افقی سایه :

Minus (left) -- 0 -- plus (right)

عدد دوم : موقعیت عمودی سایه : 

Minus (top) -- 0 -- plus (bottom)

عدد سوم : میزان محو شدگی سایه

0 یا PLUS

مقدار اخر : رنگ سایه

مثال :

text-shadow: -20px -10px 10px red;

ایجاد سایه باکس :

دستور css : box-shadow :

Box-shadow:0px 0px 0px 0px color;

عدد اول : موقعیت افقی سایه :

Minus (left) -- 0 -- plus (right)

عدد دوم : موقعیت عمودی سایه : 

Minus (top) -- 0 -- plus (bottom)

عدد سوم : میزان محو شدگی سایه

0 یا PLUS

عدد چهارم : میزان ضخامت سایه

مقدار اخر : رنگ سایه

نکته : میتوان چندین سایه را بصورت همزمان اعمال کرد :
```css
Box-shadow:1px 2px 10px 2px gray,-1px -2px 10px 3px blue;
```
ایجاد فاصله در خط اول نوشته با css :
```css
Text-indent:20px;
```
هر چه عدد بیشتر باشد فاصله خط اول بیشتر میشود

فونت نوشته ها در css :
```css
Font-family:fontName1,fontName2;
```
مرورگر از فونت اول شروع میکند و هر فونتی در دسترسی باشد اجرا میکند

بعضی فونت ها پیشفرض در سیستم عامل وجود دارند مثل فونت Tahoma

اما بعضی فونت ها (فونت فارسی) در سیستم وجود ندارد و باید فایل انرا برای کاربر قرار دهیم

افزودن فایل فونت به صفحه وب :

چهار فرمت مشخص از فونت را دانلود میکنیم
```css
Woff , woff2 , ttf , eot
```

سپس با کد css :  @font-face فایل فونت را در صفحه لود میکنیم
```css
@font-face {

    font-family: Tanha;

    src: url('Tanha.eot');

    src: url('Tanha.eot?#iefix') format('embedded-opentype'),

         url('Tanha.woff') format('woff'),

         url('Tanha.ttf') format('truetype');

    font-weight: normal;

}
```

نحوه استفاده :
```css
body {

     font-family: Tanha;

}
```

راستچین کردن وب سایت :

دستور css : direaction
```css
Direction:rtl;

Ltr

Rtl => right to left

Ltr => left to right
```
جهت پیشفرض همه ایتم های صفحه

تنظیمات داخل تگ Head :

تنظیمات مربوط به Encoding

برای اینکه کاراکتر های فارسی به درستی نمایش داده شوند 

باید encoding فایل بر روی utf-8 تنظیم گردد

زیرا utf8 از اکثر زبان ها پشتیبانی میکند

برای مشخص سازی اطلاعات صفحه یا document از meta tag استفاده میکنیم

برای مشخص سازی encoding هم به همین صورت :
```html
 <meta charset="UTF-8">
```
متا تگ توضیحات صفحه وب (قابل استفقاده توسط موتور های جستجو):
```html
<meta name="description" content="دوره های آموزشگاه فلان">
```
متا تگ کلمات کلیدی (قابل استفقاده توسط موتور های جستجو):
```html
<meta name="keywords" content="HTML, CSS, JavaScript,ICDL,ICDL2">
```
متا نگ author برای مشخص سازی نویسنده صفحه (برای موترو جستجو , برای شبکه های اجتماعی)
```html
<meta name="author" content="Ali">
```
متا تگ viewport : برای فعال سازی responsive و مشخص سازی میزان زوم صفحه در حالت responsive و سایر تنظیمات ....
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
بدون این متا تگ نسخه کامئویتر در موبایل اجرا میشود و مدیا کویری ها به درستی کار نمیکنند

ایجاد تصویر در صفحه وب :

تگ html  img
```css
-  Empty

-  Inline-block
```

```html

<img src="آدرس عکس" alt="نوشته ای که در صورت عدم لود تصویر نمایش داده میشود" title="عنوان تصویر در زمان قرار گیری موس">
```

نحوه آدرس دهی  فایل (تصاویر -- فونت -- موسیقی -- ویدیو ....)

انواع آدرس فایل در کامپیوتر :

آدرس دهی مطلق -- absolute :
```html
https://mftcdn.ir/files/lessonimages/6ieWQkjt54oHOD4z.png

C:\Users\Student\Desktop\webpack-s4-friday\img\1.jpg
```
آدرس دهی نسبی -- relative :

آدرس در این روش از محل قرار گیری فایل حاوی کد محاسبه میگردد 

img/s12.jpg

نکته مهم : در ابتدای ادرس نسبی از / استفاده نکنید

زیرا آدرس از root درایو محاسبه میشود

/img/01.jpg

نکته : margin-right , margin-leftبا مقدار auto روی ایتم های block level اجرا میشود

راه حل : قرار دادن تصویر در یک تگ block level

راه حل 2 : تغییر گروه تگ 

Display:block;

با دستور display میتوان گروه تگ مد نظر را تغییر داد

نکته : تگ های inline-block از جمله img پیشفرض یک فاصله دیفالت از هم دارند

راه حل : در html در یک خط نوشته شوند تا فاصله از بین برود

راه حل 2 : float

نکته : به هیچ عنوان هم زمان به تصویر width و height ثابت ندهید

راه حل : یا فقط height یا فقط width را مشخص کنید تا قسمت مقابل بسته به اندازه تصویر خودکار مشخص شود

نحوه ساخت خط در اطراف آیتم ها

دستور css به نام border
```css
Border:1px type color;

1px => هر عددی

Type => 

Solid -> ممتد

Dashed -> خط چین

Dotted -> نقطه چین

Color => هر رنگی
```

جهت border :
```css
Border-left:1px solid red;

Border-right:1px solid blue;

Border-top:....;

Border-bottom:...;
```

سایر دستورات border
```css
Border-style:solid;

Border-left-style:solid;

Border-right-style:solid;

Border-top-style:solid;

Border-bottom-style:solid;

Border-color:red;
```
برای چهار طرف
```css
Border-width:1px;
```

برای هر چهار طرف

نحوه ساخت مثلث در css

دستورالعمل : 

یک div دارای اندازه صفر در صفر با چهار border ضخیم بسازیم

یک border را انتخاب میکنیم روبرویی را ئاک میکنیم

دو border دیگر را بی رنگ میکنیم -- transparent
```html
<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta http-equiv="X-UA-Compatible" content="IE=edge">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Document</title>

    <style>

        *{

            margin:0;

        }

        #tri {

            width:0;

            height: 0;

            border-left: 50px solid orange;

            border-top: 50px solid transparent;

            border-bottom: 50px solid transparent;

        }

    </style>

</head>

<body>

    <div id="tri">

    </div>

</body>

</html>
```
مشابه ترفند بالا در سایت https://codepen.io/ ,  https://css-tricks.com/ موجود است

گرد سازی گوشه های آیتم

دستور css : border-radius

Border-radius:50px;

50px => میزان گردی گوشه ها 

اعمال بر روی یک طرف از border

Border:20px 20px 20px 20px;

اولین عدد گوشه بالا سمت چپ و باقی اعداد ساعت گرد مشخص میشوند

همینطور میتوان با دستور مجزا به هر طرف border-radius مجزا اعمال کرد

مثال :
```css
border-top-left-radius: 50%;

border-bottom-right-radius: 50%;

margin : حاشیه خارجی

Padding : حاشیه داخلی

Padding باعث میشود یک حاشیه همرنگ باکس در داخل باکس ایجاد شود که محتوای باکس نمیتوانند وارد این حاشیه بشوند
```
در نتیجه padding اندازه باکس را زیاد میکند

Box Model : به نحوه و ترتیب قرار گیری margin padding border در اطراف box میگوییم box model

نحوه جلوگیری از تاثیر padding روی اندازه box : 

راه حل ساده : کم کردن padding از widthیا height

راه حل اصلی : استفاده از دستور box-sizing

Box-sizing:border-box;

باعث میشود محاسبه اندازه باکس از border شروع شود
```css
 *{

            margin:0;

            padding: 0;

            box-sizing: border-box;

        }
```

Padding:50px; چهار طرف

Padding:0 20px; 

0 -> بالا و پایین

20px -> چپ و راست

Padding-right:20px; راست

Padding-left

Padding-top

Padding-bottom

Padding:10px 20px 30px 20px;

بالا راست پایین چپ

دستورات padding از نظر انواع کد نویسی مشابه هم هستند

Pseudo Classs : 

شبه کلاس ها :

هر pseudo class درای کاربرد متفاوتی است اما اکثر انها برای انتخاب آیتم های html استفاده میشود

:hover

این pseudo class استایل های ایتم در زمان قرار گیری موس روی آنرا مشخص میکند

نحوه نوشتن psudo class :
```css
Selector:hover {

//code

}

مثال

.articles:hover {

Box-shadow:2px 3px 3px 1px gray;

}

مثال :

   .articles {

            width:90%;

            height: auto;

            background-color: white;

            margin-right: auto;

            margin-left: auto;

            margin-bottom:20px;

            border-radius: 40px;

            box-shadow: 0 0 3px 1px white;

        }

        .articles:hover {

            box-shadow: 2px 2px 5px 2px white;

            border-radius: 5px;

        }
```
دستور pseudo class : first-child

این دستور اولین فرزند تگ را انتخاب میکند

:last-child

انتخاب آخرین فرزند

مثال :

p:last-child {

            background-color: red;

        }

:nth-child(2)

انتخاب فرزند n ام

p:nth-child(4){

            background-color: blue;

        }

:nth-child(2n)

انتخاب فرزند های زوج

  p:nth-child(2n){

            background-color: pink;

        }

:nth-child(2n+1)

انتخاب فرزند های فرد

 p:nth-child(2n+1){

            background-color: purple;

        }

:nth-last-child(2)

انتخاب فرزند n ام از آخر

  p:nth-last-child(2){

            background-color: orange;

        }

:last-of-type

انتخاب آخرین تگ از نوع خودش

مثال :

p:last-child {

            background-color: red;

        }

:nth-of-type(2)

انتخاب تگ n ام

p:nth-child(4){

            background-color: blue;

        }

:nth-of-type(2n)

انتخاب تگ  های زوج

  p:nth-child(2n){

            background-color: pink;

        }

:nth-of-type(2n+1)

انتخاب تگ  های فرد

 p:nth-child(2n+1){

            background-color: purple;

        }

:nth-last-of-type(2)

انتخاب تگ  n ام از آخر

  p:nth-last-of-type(2){

            background-color: orange;

        }

دستور css : opacity

تعیین میزان شفافیت آیتم (حالت شیشه ای)

عددی بین 0 تا 1 میگیرد

هر چه عدد بالاتر باشد آیتم شفافیت کمتری دارد

مثلا 0.5

مثال :

 .articles > img {

            width:100%;

            height: 100px;

            border-top-left-radius: 40px;

            border-top-right-radius: 40px;

            opacity: 0.5;

        }

        .articles:hover > img {

            opacity: 1;

        }

ساخت لیست :

برای ساخت لیست در html از دستور ul و li و ol استفاده میکنیم

Li => list item -> block

Ul => unordered list -> inline-block

Ol => ordered list

برای ساخت لیست بسته به نوع لیست که دارای ترتیب باشد یا نباشد

یکی از تگ های ol یا ul را بنویسیم

بصورت پیشفرض ol در کنار آیتم ها عدد قرار میدهد

و ul در کنار آیتم ها دایره توپر قرار میدهد

نکته : برای برداشتن دایره یا اعداد پیشفرض از دستور زیر استفاده میکنیم :

 list-style-type: none;

این تگ ها container هستند

سپس در داخل ul به تعداد آیتم هایمان li قرار میدهیم

<ul>

<li>Contact</li>

<li>About</li>

</ul>

برای تغییر استایل کنار آیتم های لیست میتوانیم از مقادیر دستور :

List-style-type:square; مربع

Circle دایره

Lower-roman اعداد رومی کوچک

Upper-roman اعداد رومی حروف بزرگ

Decimal عدد

......

برای تعریف عکس به عنوان استایل :

List-style-image:url(ادرس عکس);

Transition (دستورات css)

در تغییرات استایل آیتم های صفحه (مثال : تغییر استایل در زمان hover) دستور transition میتواند زمان , سرعت و .... تغییرات را کنترل کند

Transition-duration : مدت زمان اجرای تغییرات را مشخص میکند

Transition-duration:2s; 

Transition-duration:2000ms;

Transition-duration:2.5s;

نکته : دستورات transition باید در استایل های اصلی آیتم قرار بگیرند برای مثال اگر در هاور قرار بگیرند فقط در زمان قرار گیری موس روی آیتم اجرا میشوند

Transition-delay : تاخیر در اجرای تغییرات

Transition-delay:2s;

Transition-property : دستورات css (تغییرات css) که شمال transition میشوند

Transition-property:all; -> default value

Transition-property:width,height; => تغییرات فقط روی این دو دستور شامل transition بشوند

Transition-timing-function : رابطه زمان اجرای transition و سرعت اجرای آن

Linear : خطی => سرعت یکنواخت در زمان اجرای تغییرات

Ease-in : شروع کند و افرایش سرعت به مرور زمان

Ease -out : سرعت تغییرات به مرور کند میشود

Ease-in-out : کند -- سریع -- کند

Ease : کند -- سریع -- کند  ->default value

خلاصه نویسی transition :

Transition: property duration timing-function delay;

Transition: property duration timing-function;

Transition: property duration delay;

Transition: duration;

مثال : 

transition: width 4s ease,height 4s linear 4s,background-color 8s;

Transition: property duration timing-function delay,property duration timing-function delay,property duration timing-function delay;

Line-height : برای تعیین ارتفاع خط استفاده میشود

هر عددی در line-height قرار دهیم نصف آن برای بالای خط و نصف آن برای پایین خط اعمال میشود

برای وسط قرار دادن خط ارتفاع باکس .الد را به line-height میدهیم

نکته : در زمان هاور (یا هر سودو کلاس دیگری ) میتوان کد های جدید را بر روی فرزندان تگ هاور شده اجرا کرد
```css
selector:hover > tagName {

// css

}

مثال : 

#box:hover > p {

// css

}
```

دستور position : 

دستور زبان css میباشد

با استفاده از این دستور میتوان موقعیت قرار گیری آیتم در داخل صفحه را تعیین نمود

مقادیر دستور position : 
```
Position:static; => default value
```

موقعیت ثابت : در این حالت امکان جابجایی آیتم وجود ندارد
```
Relative
```

موقعیت نسبی : در این حالت موقعیت مکانی آیتم نسبت به تگ والد و تگ های اطراف مشخص میشود

در این جابجایی محل اولیه آیتم رزرو باقی میماند و آیتام های دیگر این فضا را اشغال نمیکنند
```
Absolute
```

موقعیت مطلق : در این حالت موقعیت نسبت به viewport یا تگ body مشخص میشود

. هیچ ارتباطی با تگ های اطراف خود ندارد

پس از جابجایی محل اولیه توسط ایتم های دیگر اشغال میشود
```
Fixed
```

موقعیت ثابت نسبت به اسکرول صفحه : مثل absolute است اما در زمان اسکرول نسبت به اسکرول صفحه موقعیت ثابت دارد
```
Sticky
```

موقعیت چسبنده : *  یادآوری

در دستور position باید مختصات قرار گیری را با دستورات :
``
Top:200px;

or

Bottom:200px;

Right:200px;

or

Left:200px;
```

مثال :
```
Position:absolute;

Left:200px;

Top:200px;
```

نکته : تمامی مختصات ها مقدار منفی میگیرند

تمرین اول : منو های social media بصورت کشویی

در سمت چپ صفحه یکسری آیکون نمایش میدهیم که در زکمان قرار گیری موس روی آنها 

بصورت کشویی باز میشون دو اسم سوشال مدیا نمایش داده میشود

منابع تمرین :

آیکون از https://icons8.com/

نمونه : https://codepen.io/jithinta/pen/VwLZEKE

تگ های ساختاری  semantic در html :

بجای اینکه همه قسمت های سایت را با div ایجاد کنیم از این تگ ها استفاده میکنیم

تا هر قسمت معنا دار تر شود (هر نرم افزاری که کد را بررسی میکند)

Header

سربرگ یک قسمت یا کل سایت

Footer

پانوشت هر قسمت یا کل سایت

Main

محتویات اصلی سایت

Article

محتویات اصلی سایت شامل خبر , مقاله , محصول (به ازای هر کدام)

Aside

محتویاتی که محتوای اصلی صفحه نیستند (فرم ورود, تبلیغات, یا معمولا سایدبار .....)

Nav

منوی ناوبری سایت

Section

ایجاد بخش مجزا در صفحه

Address

آدرس محل شرکت یا هر آدرس دیگری

Q

نقل قول تک خطی 

Blockquote

نقل قول چند خطی

Figure

Figcaption

مدیا و توضیحات آن
```html
<div>

<img src=""/>

<p>description</p>

</div>

<figure>

<img src="">

<figcaption>Description</figcaption>

</figure>
```

نحوه تشخیص :

ساخت انیمیشن در css :

1.  برای ساخت انیمیشن باید ابتدا برای انیمیشن یک نام مشخص کنیم
```css
Animation-name:myanimation;
```

نکته : اسم انیمیشن و سایر دستورات آنرا در تگی قرار میدهیم که قرار است انیمیشن بر روی آن اجرا شود

2 . مشخص سازی مدت زمان اجرای انیمیشن
```css
Animation-duration:2s;
```

3 . مشخص سازی فریم های انیمیشن
```css
@keyframes mycircle {

            from {

                left: 0;

                top:0;

            }

            to {

                left:50%;

                top:50%;

            }

        }
```
مشخص سازی بیشتر از یک فریم با درصد :
```css
        @keyframes mycircle {

            0% {

                left: 0;

                top:0;

            }

            25%{

                left:50%;

                top:50%;

            }

            50%{

                left:80%;

                top:80%;

            }

            75%{

                left:200px;

                top:600px;

            }

            100% {

                left:0;

                top:0;

            }

        }
```	

نکته : هر دستور css ای در داخل فریم های قابل قرار گیری است

تعداد فعات اجرای انیمیشن :
```css
Animation-iteration-count:1;

Animation-iteration-count:100;

Animation-iteration-count:infinite; بینهایت
```

ترکیب position های absolute , relative
```
Relative
```

جای خالی ایتم رزرو باقی میموند

نسب به تگ پدر جابجا میشوند
```
Absolute
```

جای خالی رزرو باقی نمیماند و روی آیتم های میافتد

نسبت به تگ body جابجا میشود

نحوه ترکیب :

به تگ پدر relative و به فرزند ها absolute میدهیم در این حالت تگ های فرزرند ترکیب خصوصیات سبز رنگ را دارا هستند

نکته : اگر آیتمی در جهت مخالف direction صفحه از صحه خارج شود باعث ایجاد اسکرول افقی میشود

راه حل : جلوگیری از خروج ایتم از تگ پدر با اعمال دستور overflow:hidden

هدایت کاربر به صفحات دیگر در وب :

برای اینکار از تگ a استفاده میکنیم
```html
<a href="">About</a>
```

مهمترین attribute href میباشد

در این قسمت آدرس محل هدایت کاربر مشخص میشود

که میتواند آدرس نسبی یا مطلق باشد

مثال :
```
http://google.com

about.html

/pages/contact.html
```

نکته : تگ a میتواند بر روی هر نوع ایتمی رار بگیرد مثل نوشته یا تصویر یا div و ....

مثال :
```html
<nav id="navbar" class="container">

        <ul>

            <li>

                <a href="index.html">Home</a>

            </li>

            <li>

                <a href="about.html">About</a>

            </li>

            <li>

                <a href="contact.html">Contact</a>

            </li>

            <li>

                <a href="news.html">News</a>

            </li>

        </ul>

    </nav>
```
نکته : تگ A بصورت دیفالت یک استایل COLOR:BLUE; و text-decoration:underline; به نوشته اعمال میکند
```css
  #navbar > ul > li > a {

            text-decoration: none;

        }
```

مشخص سازی نحوه باز شدن لینک :

لینک میتواند در تب جدید باز شود
```
Attribute target
```

```html
<a target="_self" href="index.html">same tab</a>

<a target="_blank" href="index.html">new tab</a>
```

اگر target بر روی _blank باشد صفحه در تب جدید باز میشود

دستورات git :
```
Git clone repository_url
```

دریافت clone پروژه گیت
```
Git status
```

مشاهده وضعیت فایل ها در git
```
Git add .
```

با این دستور فایل های جدید به flow git اضافه میشوند

میش.د بجای . اسم فلدر یا فایل را قرار داد

بعد از add کردن فایل ها باید دبرای ارسال یا push کد برای کد ها یک کامیت حاوی عنوان علت تغییرات مشخص کنیم
```
git commit -m "message of commit"
```

نکته : قبل commit باید مشخص کنیم چه کسی هستیم
```
  git config --global user.email "you@example.com"

  git config --global user.name "Your Name"
```
