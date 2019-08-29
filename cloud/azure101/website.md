# สร้างเว็บตัวแรกกัน

## 🤔 มี Resource group ละทำไรต่อดี ?

คราวนี้เราจะมาลองสร้างเว็บใช้ฟรีกันบน Microsoft Azure ดูบ้าง ซึ่งการสร้างเว็บมันเหมือนกับเป็นโปรแกรม Hello world นั่นแหละ! งั้นเราไปลุยกันว่าจะง่ายสมคำพูดไหม

{% hint style="info" %}
**Azure Portal**  
จะทำตามในรอบนี้ให้เข้าไปที่ [https://portal.azure.com](https://portal.azure.com) เน่อ  
ส่วนถ้าใครยังไม่ได้สมัครก็ไปสมัครให้เรียบร้อยแซ๊ร [\(วิธีสมัครจิ้มตรงนี้\)](https://saladpuk.gitbook.io/learn/cloud/azure101/register)
{% endhint %}

## 🤔 สร้างเว็บบนคลาว์ทำไง ?

1.ที่เมนูด้านซ้ายมือให้เลือก Resource groups ซะ แล้วในหน้าตรงกลางให้เลือกชื่อ Resource group ที่เราสร้างไว้

![](../../.gitbook/assets/image%20%2873%29.png)

2.หลังจากที่เข้ามาใน Resource group แล้วให้กดปุ่ม + ที่มุมบนซ้ายของเมนู

![](../../.gitbook/assets/image%20%2819%29.png)

3.ระบบจะพาเราไปที่หน้า **Marketplace** ซึ่งในหน้า marketplace นี้เป็นหน้าหลักในการเลือก service ที่เราจะทำการสร้าง แต่ในกรณีของเราขี้เกียจหา เลยพิมพ์ในช่องค้นหาว่า **Web App** แล้วกด enter

![](../../.gitbook/assets/image%20%2812%29.png)

4.Azure จะแสดงรายละเอียดของ service ที่เราเลือกขึ้นมา ซึ่งในกรณีนี้คือ Web App โดยให้คำแนะนำเบื้องต้นว่ามันคืออะไร เล่นอะไรได้บ้าง ราคาเท่าไหร่ บลาๆ ซึ่งถ้าอ่านเสร็จแล้วให้กดปุ่ม **Create** สีน้ำเงินไดด้เบย

![](../../.gitbook/assets/image%20%2857%29.png)

5.ขั้นตอนถัดมาเขาก็จะถามรายละเอียดของเว็บที่เราจะเขียนต่างๆ ก็ค่อยๆเลือกใส่ทีละอันเลย แล้วพอใส่เสร็จก็กดปุ่ม **Review and create** โลด

| ชื่อ | รายละเอียด |
| :--- | :--- |
| **Resource Group** | เว็บนี้จะสร้างใน resource group ไหน |
| **Name**  | ชื่อเว็บอะไร ซึ่งชื่อจะต้องไม่ซ้ำกันคนอื่นทั่วโลก |
| **Runtime stack** | เราจะให้มัน support อะไรบ้าง เช่น php, java, phython, node, .net core |
| **Operating System** | ระบบปฏิบัติการจะเป็นตัวไหน |
| **Region** | เว็บนี้จะตั้งอยู่โซนไหน |
| **App Service Plan** | จะให้เขาเก็บเงินเราแบบไหน \(ถ้ากลัวเสียเงินก็เลือกเป็น Free F1 นะครับ ฟรีตลอดกาล\) |

![](../../.gitbook/assets/image%20%2850%29.png)

{% hint style="info" %}
**App Service Plan**  
รายละเอียดเรื่องการเก็บเงินของ Microsoft Azure อยู่ในวีดีโอด้านล่างสุดนะ ถ้าสนใจลองเข้าไปดูได้ราวๆนาทีที่ 3:48 งับ
{% endhint %}

6.สุดท้ายเขาก็จะถามยืนยันว่าจะสร้างเว็บนี้จริงหรือเปล่า ทำมาขนาดนี้แล้วจะกดยกเลิกเหรอครับ **Create** สีฟ้าๆอะจิ้มโลด

![](../../.gitbook/assets/image%20%289%29.png)

7.รอจนกว่าจะเสร็จครับ ก็เป็นอันเสร็จพิธี

![](../../.gitbook/assets/image%20%2827%29.png)

## 🤔 สร้างเสร็จแล้วไงต่อ ?

1.ก็ลองไปเล่นสิครับ โดยให้เราเข้าไปที่ resource group ที่สร้างไว้ แล้วเราจะเห็นเว็บตัวนั้นอยู่ ให้กดมันเบา 1 ครั้ง

![](../../.gitbook/assets/image%20%2868%29.png)

2.หลังจากนั้นให้กดปุ่ม **Browse** ที่เมนูด้านบนฮั๊ฟ

![](../../.gitbook/assets/image%20%2837%29.png)

3.แล้วเว็บของเราก็จะโผลมาแว๊วววว ซึ่งหน้าตาเว็บจะเป็น default ที่ Microsoft เตรียมไว้ให้เรา \(หน้าตาเว็บอาจจะไม่เหมือนของผมนะ เพราะ Microsoft เปลี่ยนหน้า default นี้บ่อยอยู่ครับ\)

![](../../.gitbook/assets/image%20%2870%29.png)

{% hint style="info" %}
**URL**  
ตัวเว็บของเราจะมี url เป็น **https://ชื่อเว็บที่ตั้ง.azurewebsites.net** เสมอ ซึ่งเราสามารถเปลี่ยนได้ในภายหลังนะครับ ส่วนวิธีเปลี่ยนจะอยู่ในคอร์ส **Azure Service Specific** ดูได้จาก side menu นะครับ
{% endhint %}

## 🎥 วีดีโอการสร้างเว็บไซต์

{% embed url="https://www.youtube.com/watch?v=vBYty\_wGdpQ&list=PLUjAn8nwWniiReiOqUqYwxG7ny2bhENMg&index=7" %}

## 🤔 อยากเปลี่ยนหน้าตาเว็บทำไงอ่ะ ?

สามารถทำได้หลายวิธีเลย เช่น **FTP, GitHub, CI/CD** บลาๆ ซึ่งในตัวอย่างนี้ผมขอทำแบบง่ายผ่าน FTP ไปก่อนนะครับ ส่วนถ้าสนใจการอัพเดทแบบอื่นๆ ดูได้ในคอร์ **Azure Service Specific** ดูได้จาก side menu นะครับ

{% embed url="https://www.youtube.com/watch?v=N6vHoLLp3As&list=PLUjAn8nwWniiReiOqUqYwxG7ny2bhENMg&index=7" %}
