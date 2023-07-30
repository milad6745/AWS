# چیست aws 
- یک infra stracter as service است یعنی تمامی موارد شامل ست کردن آیپی و گرفتن منابع و ... توسط سرویس و با چند کلیک انجام میشود
- دیتای Ec2 به روش های مختلفی ذخیره سازی میشه که بصورت پیشفرض EBS استفاده میکند.
- سرویس Ec2 مثل یک هسته پردازشی است که تمامی منابع را دارد هارد رم cpu , ..
- این سرویس EC2 دارای سرویس Auto Scaling است و در صورتی که بخاهیم میتوانیم تعداد Ec2 هایمان را افزایش دهیم اگر سی پی یو افزایش پیدا کرد
   و به فلان قدر رسید تعداد ECU ها را افزایش بده
 - برای تعادل بار از elastic load balancer میتوانیم استفاده کنیم

## ویژگی های Ec2

 - ای سی 2 ها هم مثل ورچوال ماشین ها شامل OS , ram , CPU , storage
- انواع استوریج هایی که EC2 استفاده میکند : EBS , EFS (network attach)
- استوریج دیگر ECS است که مدل سخت افزاری است (بصورت هاردوری است)
-   نت ورک کارت دارد
- دارای فایروال است (security group)
- دارای Ec2 user data مثله مبخاهیم یه لینوکس نصب کنیم و همزمان برای شما پایتون و مونگو و ... را برای ما نصب کند . برای این کار کد ها
را داخل Ec2 user data  قرار میدهیم و خودش نصب میکند.
## در مورد naming convention
- 
- family class / class t
- generation / 2
- size / micro
-
-  example : t2 micro -- > free instance (750H per month) -> class 1 با توان پردازشی پایین
-  example : m5.2xlarge

## EC2 class
- balance performance (t,m) -->
- compute optimize --> batch procecing , high performance
- memory optimize --> large data memory,no sql db, in memory DB
- storage performance -- > high read / write , nosql db ,

  ## Securoty Group
  ![image](https://github.com/milad6745/AWS/assets/113288076/28617f90-bb16-44a1-9421-79bcf27cf88c)
- این ماژول خارج از Ec2 قرار گرفته و ترافیک ورودی و خروجی را کنترل میکند.
- برای ورود ترافیک باید Allow rule تعریف شده باشد در غیر این صورت Deny میشود.
- این ویژگی Statefull است و در حالت عادی ترافیک برگشتی Allow آست .
- برای اینکه دو سکیوریتی گروپ را با هم Allow کنیم میتوانیم از آیپی و یا نام Security Group آستفاده نمایید .
  
  
  
  
  
