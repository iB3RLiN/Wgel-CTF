# Wgel-CTF
Wgel CTF 

اول شي نعمل سكان للمنافذ والخدمات اللي شغالة على السيرفر

![nmap](https://user-images.githubusercontent.com/73380139/182121920-2c12bf28-1c02-415b-ae4e-8f35ddd27c78.png)


نشوف المسارات المخفية ونلاحظ مسار مثير للاهتمام

![dirb](https://user-images.githubusercontent.com/73380139/182121950-e2819958-2669-49bb-92a7-003ebef81b06.png)


بعد تتبع المسار نلقى مفتاح
rsa!
هذا اول خيط راح يمكنا من اختراق الهدف لكن الى الان ما نعرف هذا المفتاح يخص مين بالضبط

![RSAkey](https://user-images.githubusercontent.com/73380139/182135975-9f1621c3-831f-4b2c-9642-22f36e4c7b18.png)

يعد التدقيق في صفحات الموقع نلاحظ وجود تعليق يطلب من شحص معين تحديث الموقع 

![findName](https://user-images.githubusercontent.com/73380139/182136634-9319aad6-cb80-4656-953d-b68ed1196d3f.png)

راح نجرب اسم المسؤل عن تحديث الموقع مع المفتاح اللي حصلته في المسار المخفي ونحاول 
![mvRSA](https://user-images.githubusercontent.com/73380139/182137078-483daea6-f2d2-422f-873f-999fed965dc4.png)

نجحنا ووصلنا لـ العلم الخاص باليوزر
![catUserFlag](https://user-images.githubusercontent.com/73380139/182137467-65af0715-6c5c-4de1-8f47-51330d52c50b.png)

لكن لما نحاول نوصل للروت نشوف اننا ما نملك صلاحيات بس لو تلاحظ ان في ثغرة تسمح لنا نوصل للروت من خلال 
Wget
وراح نجربها

![PrivRoot](https://user-images.githubusercontent.com/73380139/182137751-17a79042-9e19-41d2-a2c8-825a306f6b4d.png)

نطلب الملف من خلال 
Wget 

![wget](https://user-images.githubusercontent.com/73380139/182138467-ed1ea0b9-3bba-4f8e-b19f-8de84ae2cf9e.png)


نفتح اتصال نت كات على نفس البورت وراح نحصل على العلم الخاص بالروت
![rootFlag](https://user-images.githubusercontent.com/73380139/182139107-491e836a-e3f6-4c68-9ae3-e795f6cc4520.png)





