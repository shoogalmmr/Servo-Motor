# سيرفو موتر
## المتطلبات
اردوينو Arduino UNO 

6 محركات سيرفو

مصدر طاقة مناسب ( مزود بطاقة )

أسلاك توصيل

لوحة توصيل (Breadboar) 

## اعداد الدائره 
### توصيل أسلاك إشارة التحكم لمحركات السيرفو إلى Arduino:

توصيل أسلاك إشارة التحكم (التي بلون البرتقالي) لمحركات السيرفو إلى دبابيس التحكم الرقمي على Arduino:

المحرك 1: إلى الدبوس 4 على Arduino

المحرك 2: إلى الدبوس 5 على Arduino

المحرك 3: إلى الدبوس 6 على Arduino

المحرك 4: إلى الدبوس 7 على Arduino

المحرك 5: إلى الدبوس 8 على Arduino

المحرك 6: إلى الدبوس 9 على Arduino

### توصيل اسلاك vcc  و GND 

توصيل سلك vcc (اللون الاحمر) في منفذ 5v المتواجد في الاردوينو Arduino ثم ايصاله بلوحه التوصيل على الموجب ؛كذلك نقوم بتوصيل جميع اسلاك الخاصه بالمحركات في لوحه التوصبل Breadboar

توصيل سلك GND (اللون الاسود او البني) من منفذ GND في الاردينو Arduino الى لوحه التوصيل عللى السالب ؛ كذلك نقوم بتوصيل جميع اسلاك الخاصه بالمحركات في لوحه التوصبل Breadboar

## الصوره التخطيطيه
صوره التخطيطيه لتوصيل محركات السيرفو بـ Arduino باستخدام لوحة التوصيل Breadboar:

<img src= "https://github.com/user-attachments/assets/d7919b17-ebce-401b-af00-f8cbfb3d608e" width="900" height="500">

## الكود البرمجي
الكود لتشغيل المحركات 
```
#include <Servo.h>


Servo servo1;
Servo servo2;
Servo servo3;
Servo servo4;
Servo servo5;
Servo servo6;

void setup() {
  
  servo1.attach(4);
  servo2.attach(5);
  servo3.attach(6);
  servo4.attach(7);
  servo5.attach(8);
  servo6.attach(9);
}

void loop() {
  
  testServos();
}

void testServos() {
  
  servo1.write(45);
  servo2.write(45);
  servo3.write(45);
  servo4.write(45);
  servo5.write(45);
  servo6.write(45);
  delay(1000); 

  
  servo1.write(135);
  servo2.write(135);
  servo3.write(135);
  servo4.write(135);
  servo5.write(135);
  servo6.write(135);
  delay(1000); 
}


```
