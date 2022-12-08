# Supervised Learning

คือการเรียนรู้จากโจทย์(Input) และ เฉลย(Output) เช่นการมีชุดค่า $x$ ที่มีคำตอบเป็น  $y$ จำนวนหนึ่งแล้ว supervised machine learning จะต้องหาความสัมพันธ์ระหว่าง $x$ และ $y$ และจะต้องทำนายค่า $x$ ที่ไม่เคยเจอได้อย่างแม่นยำ

 ตัวอย่าง

| Input (⁍) | Output (⁍) | Application |
| --- | --- | --- |
| Email | spam? (0/1) | spam filtering |
| audio | text transcripts | speech recognition |
| English | Thai | machine translation |
| ad, user info | click? (0,1) | online advertising |

<aside>
💡 **Notation**

ก่อนจะเริ่มลงรายละเอียดของ Supervised Learning ผู้เขียนขอสร้างความเข้าใจเกี่ยวกับ notation ให้ไปในทิศทางเดียวกันก่อน

| ⁍ | input | feature |
| --- | --- | --- |
| ⁍ | output | target |
| ⁍ | estimated ⁍ | prediction |
| ⁍ | จำนวนตัวอย่าง
สำหรับการ train |  |
| ⁍ | ชุดตัวอย่าง
สำหรับการ train |  |
| ⁍ | ชุดตัวอย่าง
สำหรับการ train ตัวที่ ⁍
⁍ |  |
</aside>

## Linear Regression Model (with univariate)

ลำดับการทำงานคร่าวๆ

```json
		training set

				⬇️

	learning algorithm

				⬇️

			model (f)
```

จาก model ทีได้มาเราก็จะสามารถนำค่า  $x$ ที่อยู่นใน training set หรือไม่อยู่ก็ได้ มาป้อนใส่ model ของเราเพื่อให้ model ทำนายค่า $\hat{y}$

$x → f_{(model)} → \hat{y}$

**แล้ว $f$ คืออะไรล่ะ?**

$$
f_{w,b}(x) = wx+b
$$

$f$ คือ Linear function ที่มี $x$ เป็น input ขึ้้นอยู่กับ $w$ กับ $b$ และให้ผลลัพธ์เป็น $\hat{y}$ หรือที่เรียกกันทั่วไปว่า Linear Regression Model

Model ที่กล่าวไปข้างต้้นเป็นเพียง model สำหรับ 1 ตัวแปลเท่านั้น หรือเรียกว่า Univariate Linear Regression Model (Univariate = one variable)