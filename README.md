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

@media only screen and (min-width:768px){
	کد سی اس اس
}
کد سی اس اس بالا در صفحات 768 به بالا اجرا میشود
@media only screen and (max-width:768px){
	کد سی اس اس
}
کد سی اس اس بالا در صفحات 768 به پایین اجرا میشود

@media only screen and (min-width:768px) and (max-width:1170px){
	کد سی اس اس
}
صفحات بین 768 الی 1170

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



چیشن آیتم ها در css
دستور float  در  css : با استفاده از این دستور میتوانیم ایتم ها به سمت راست یا چپ بصورت افقی بچینیم
Float:left;
Float:right;
Float:none;
دستور float باعث میشود آیتم ها از layout تگ پدر خارج شوند
راه حل : تنظیم ارتفاع ثابت برای تگ پدر
راه حل 2 : یک div خالی بعد آیتم های دارای float میسازیم و به آن دستور clear:right; یا clear:left; یا  clear:both; برای زمانی که هر دو float وجود دارند 

این دستور مشکل float را حل میکند

ایجاد عنوان در وب سایت
برای ساخت عنوان از تگ های html زیر استفاده میکنیم
<h1></h1>
….
<h6></h6>

تفاوت عناوین :
تفاوت اول : سایز : هر چه عدد تگ کوچکتر باشد سایز عنوان بزرگ تر است (با دستور font-size میتوان سایز انهارا عوض کرد)

تفاوت دوم : اهمیت عنوان : هر چه عدد کوچکتر باشد عنوان مهمتر است

اهمیت از نظر SEO است (مخفف Search engine optimize به فارسی بهینه سازی سایت برای موتور جستجو)


انتخاب تگ html بر اساس تگ parent در CSS
Parent > child {
	//css
}

این انتخاب میتواند تا بی نهایت ادامه ئیدا کند :
 Parent > parent > parent > child {
	
}


تایپوگرافی متن در css و html
تغییر رنگ نوشته :
Color:red;
تغییر سایز فونت نوشته :
Font-size:22px;
نوشته بولد (ضخامت نوشته)
 1 . <b>  Text  </b>
2. <strong> Text </strong>
هر دو نوشته را بولد میکنند و در ظاهر هیچ تفاوتی ندارند
منتها تگ strong اهمیت نوشته را از نظر seo افزایش میدهد
3. font-weight:100;
100
200
300 -> lighter
400 -> normal
500
600
700 -> bold
800
900 => bolder

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
<i> Text </i>
<em> Text </em>
هر دو نوشته را italic  میکنند و در ظاهر هیچ تفاوتی ندارند
منتها تگ em  اهمیت نوشته را از نظر seo افزایش میدهد
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
<del> 	 </del> Text
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
Minus (left) – 0 – plus (right)
عدد دوم : موقعیت عمودی سایه : 
Minus (top) – 0 – plus (bottom)
عدد سوم : میزان محو شدگی سایه
0 یا PLUS

مقدار اخر : رنگ سایه
مثال :
text-shadow: -20px -10px 10px red;


ایجاد سایه باکس :
دستور css : box-shadow :
Box-shadow:0px 0px 0px 0px color;


عدد اول : موقعیت افقی سایه :
Minus (left) – 0 – plus (right)
عدد دوم : موقعیت عمودی سایه : 
Minus (top) – 0 – plus (bottom)
عدد سوم : میزان محو شدگی سایه
0 یا PLUS
عدد چهارم : میزان ضخامت سایه
مقدار اخر : رنگ سایه


نکته : میتوان چندین سایه را بصورت همزمان اعمال کرد :
Box-shadow:1px 2px 10px 2px gray,-1px -2px 10px 3px blue;

ایجاد فاصله در خط اول نوشته با css :
Text-indent:20px;
هر چه عدد بیشتر باشد فاصله خط اول بیشتر میشود


فونت نوشته ها در css :
Font-family:fontName1,fontName2;
مرورگر از فونت اول شروع میکند و هر فونتی در دسترسی باشد اجرا میکند
بعضی فونت ها پیشفرض در سیستم عامل وجود دارند مثل فونت Tahoma
اما بعضی فونت ها (فونت فارسی) در سیستم وجود ندارد و باید فایل انرا برای کاربر قرار دهیم


افزودن فایل فونت به صفحه وب :
چهار فرمت مشخص از فونت را دانلود میکنیم
Woff , woff2 , ttf , eot

سپس با کد css :  @font-face فایل فونت را در صفحه لود میکنیم
@font-face {
    font-family: Tanha;
    src: url('Tanha.eot');
    src: url('Tanha.eot?#iefix') format('embedded-opentype'),
         url('Tanha.woff') format('woff'),
         url('Tanha.ttf') format('truetype');
    font-weight: normal;
}

نحوه استفاده :
  body {
                    font-family: Tanha;
                }

راستچین کردن وب سایت :
دستور css : direaction
Direction:rtl;
Ltr


Rtl => right to left
Ltr => left to right
جهت پیشفرض همه ایتم های صفحه



تنظیمات داخل تگ Head :
تنظیمات مربوط به Encoding
برای اینکه کاراکتر های فارسی به درستی نمایش داده شوند 
باید encoding فایل بر روی utf-8 تنظیم گردد
زیرا utf8 از اکثر زبان ها پشتیبانی میکند
برای مشخص سازی اطلاعات صفحه یا document از meta tag استفاده میکنیم
برای مشخص سازی encoding هم به همین صورت :

 <meta charset="UTF-8">

متا تگ توضیحات صفحه وب (قابل استفقاده توسط موتور های جستجو):
<meta name="description" content="دوره های آموزشگاه فلان">

متا تگ کلمات کلیدی (قابل استفقاده توسط موتور های جستجو):
<meta name="keywords" content="HTML, CSS, JavaScript,ICDL,ICDL2">

متا نگ author برای مشخص سازی نویسنده صفحه (برای موترو جستجو , برای شبکه های اجتماعی)
<meta name="author" content="Ali">

متا تگ viewport : برای فعال سازی responsive و مشخص سازی میزان زوم صفحه در حالت responsive و سایر تنظیمات ....
<meta name="viewport" content="width=device-width, initial-scale=1.0">

بدون این متا تگ نسخه کامئویتر در موبایل اجرا میشود و مدیا کویری ها به درستی کار نمیکنند


ایجاد تصویر در صفحه وب :
تگ html  img
-	Empty
-	Inline-block

<img src="آدرس عکس" alt="نوشته ای که در صورت عدم لود تصویر نمایش داده میشود" title="عنوان تصویر در زمان قرار گیری موس">

نحوه آدرس دهی  فایل (تصاویر – فونت – موسیقی – ویدیو ....)

انواع آدرس فایل در کامپیوتر :
آدرس دهی مطلق – absolute :
https://mftcdn.ir/files/lessonimages/6ieWQkjt54oHOD4z.png
C:\Users\Student\Desktop\webpack-s4-friday\img\1.jpg
آدرس دهی نسبی – relative :
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
Border:1px type color;
1px => هر عددی
Type => 
Solid -> ممتد
Dashed -> خط چین
Dotted -> نقطه چین
Color => هر رنگی

جهت border :
Border-left:1px solid red;
Border-right:1px solid blue;
Border-top:….;
Border-bottom:…;
سایر دستورات border
Border-style:solid;
Border-left-style:solid;
Border-right-style:solid;
Border-top-style:solid;

Border-bottom-style:solid;

Border-color:red;
برای چهار طرف

Border-width:1px;
برای هر چهار طرف


نحوه ساخت مثلث در css
دستورالعمل : 
یک div دارای اندازه صفر در صفر با چهار border ضخیم بسازیم
یک border را انتخاب میکنیم روبرویی را ئاک میکنیم
دو border دیگر را بی رنگ میکنیم – transparent
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

مشابه ترفند بالا در سایت https://codepen.io/ ,  https://css-tricks.com/ موجود است

گرد سازی گوشه های آیتم
دستور css : border-radius
Border-radius:50px;
50px => میزان گردی گوشه ها 
اعمال بر روی یک طرف از border
Border:20px 20px 20px 20px;
اولین عدد گوشه بالا سمت چپ و باقی اعداد ساعت گرد مشخص میشوند
همینطور میتوان با دستور مجزا به هر طرف border-radius مجزا اعمال کرد
مثال :
border-top-left-radius: 50%;
border-bottom-right-radius: 50%;

margin : حاشیه خارجی
Padding : حاشیه داخلی
Padding باعث میشود یک حاشیه همرنگ باکس در داخل باکس ایجاد شود که محتوای باکس نمیتوانند وارد این حاشیه بشوند
در نتیجه padding اندازه باکس را زیاد میکند
Box Model : به نحوه و ترتیب قرار گیری margin padding border در اطراف box میگوییم box model 

نحوه جلوگیری از تاثیر padding روی اندازه box : 
راه حل ساده : کم کردن padding از widthیا height
راه حل اصلی : استفاده از دستور box-sizing
Box-sizing:border-box;
باعث میشود محاسبه اندازه باکس از border شروع شود
 *{
            margin:0;
            padding: 0;
            box-sizing: border-box;
        }

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
انتخاب تگ  های زوج
  p:nth-child(2n){
            background-color: pink;
        }

:nth-of-type(2n+1)
انتخاب تگ  های فرد
 p:nth-child(2n+1){
            background-color: purple;
        }

:nth-last-of-type(2)
انتخاب تگ  n ام از آخر
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
Ease-in-out : کند – سریع – کند
Ease : کند – سریع – کند  ->default value

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
selector:hover > tagName {
	// css
}
مثال : 
#box:hover > p {
	// css
}
دستور position : 
دستور زبان css میباشد
با استفاده از این دستور میتوان موقعیت قرار گیری آیتم در داخل صفحه را تعیین نمود
مقادیر دستور position : 
Position:static; => default value 
موقعیت ثابت : در این حالت امکان جابجایی آیتم وجود ندارد
Relative
موقعیت نسبی : در این حالت موقعیت مکانی آیتم نسبت به تگ والد و تگ های اطراف مشخص میشود
در این جابجایی محل اولیه آیتم رزرو باقی میماند و آیتام های دیگر این فضا را اشغال نمیکنند
Absolute
موقعیت مطلق : در این حالت موقعیت نسبت به viewport یا تگ body مشخص میشود
. هیچ ارتباطی با تگ های اطراف خود ندارد
پس از جابجایی محل اولیه توسط ایتم های دیگر اشغال میشود
Fixed
موقعیت ثابت نسبت به اسکرول صفحه : مثل absolute است اما در زمان اسکرول نسبت به اسکرول صفحه موقعیت ثابت دارد
Sticky
موقعیت چسبنده : *  یادآوری 

در دستور position باید مختصات قرار گیری را با دستورات :
Top:200px;
or
Bottom:200px;


Right:200px;
or
Left:200px;
مثال :
Position:absolute;
Left:200px;
Top:200px;

نکته : تمامی مختصات ها مقدار منفی میگیرند

تمرین اول : منو های social media بصورت کشویی
در سمت چپ صفحه یکسری آیکون نمایش میدهیم که در زکمان قرار گیری موس روی آنها 
بصورت کشویی باز میشون دو اسم سوشال مدیا نمایش داده میشود
منابع تمرین :
آیکون از https://icons8.com/
نمونه : https://codepen.io/jithinta/pen/VwLZEKE



ترتیب قرار گیری آیتم های دارای position بر روی یکدیگر :
بصورت پیشفرض هر آیتمی که آخر (در html) نوشته شود روی سایر آیتم ها قرار میگیرد
تغییر ترتیب قرار گیری :
z-index:number;
دستور z-index ترتیب قرار گیری یتم هارا مشخص میکند
هر چه عدد آن بالاتر باشد آیتم روتر قرار میگیرد
هر چه عدد پایین تر باشد آیتم زیر تر قرار میگیرد
عدد پیشفرض 0 است

کامنت comments :
کامنت قسمتی از کد است که اجرا نمیشود 
برای قرار دادن توضیحات کد و غیر فعال کردن کد های وب سایت استفاده میشود
کامنت در css :
یک خط یا چند خط : /* code */
کامنت در html :
یک خط یا چند خط : <!-- code -->
کلید میانبر کامنت کردم ctrl + / است


کد های ساخت رنگ :
کد رنگ HEX :
این کد رنگ با علامت # شروه میشود و شامل 6 کاراکتر یا عدد میباشد
#000000 => مشکلی
#ffffff => سفید
دو کاراکتر اول رنگ قرمز
دو کاراکتر دوم سبز
دو کاراکتر سوم آبی
و ترکیب میزان این رنگ ها رنگ نهایی میباشد
کاراکتر های قابل استفاده :
0 1 2 3 4 5 6 7 8 9 A B C D E F
نکته : هر چه اعداد به سمت بالا نزدیک تر باشند رنگ روشن تر است
و بالعکس رنگ تیره تر

نکته : هر چه اعداد به f نزدیک تر باشند میزان رنگ بشتر 
و بالعکس میزان رنگ کمتر است
#ff0000 => قرمز مطلق
#00ff00 => سبز
#0000ff => آبی
#ff00ff => بنفش
#f20022
کد رنگ rgb :
این رنگ با rgb شروع میشود و در داخل پرانتز سه عدد قرار میگیرد
عدد ااول رنگ قرمز
عدد دوم سبز
عدد سوم آبی
هر عدد بین 0 الی 255 میباشد
هر چه به 255 نزدیک تر باشیم روشنایی بیشتر و رنگ هم بیشتر است
و هر چه به صفر نزدیک تر باشیم روشنایی کمتر  و رنگ هم کمتر است
Rgb(0,0,0) => black
Rgb(150,0,150) => purple
کئ رنگ rgba :
که مقدار a عددی اضافه برای میزان شفافیت رنگ است
عدد بین 0 و 1
هر جه به صفر نزدیک تر اباشیم رنگ روشن تر
هرچه به 1 نزدیک تر باشیم رنگ تیره تر است
دیفالت روی 1
Rgba(150,0,150,0.5) => رنگ بنفش شیشه ای یا شفاف

کد رنگ hsl : * یادآوری

