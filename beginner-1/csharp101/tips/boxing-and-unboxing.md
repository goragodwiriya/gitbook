# 💡 Boxing & Unboxing

{% hint style="success" %}
ความรู้เรื่องนี้เป็นความรู้ประดับ ไม่รู้ก็ทำงานได้ไม่มีปัญหาอะไร แต่ถ้ารู้จะทำให้ performance ของโค้ดเราดีขึ้น ละเข้าใกล้ Production Code มาขึ้นครัช
{% endhint %}

## Boxing

ปรกติตัวแปรที่มี Data type เป็น object นั้นจะสามารถเก็บทุกสิ่งทุกอย่างใน C\# ได้ เพราะมันคือต้นตระกูลนั่นเอง เช่น ถ้าเราอยากเก็บค่าตัวเลขไว้ใน object เราก็เขียนแบบนี้ก็ได้

```csharp
int i = 123;
object o = i;     // boxing
```

ซึ่งจากโค้ดด้านบน การทำงานจริงๆของมันคือ มันจะไปสร้าง object ใหม่ให้กับตัวแปร o แล้วมันจะ **Copy** ค่าตัวแปร i ไปเก็บไว้ใน heap แล้วค่อยให้ตัวแปร o ชี้ไปหาตัวแปรที่ copy ขึ้นมาต่ออีกที

![](../../../.gitbook/assets/image%20%28241%29.png)

จากที่ร่ายมากระบวนการนี้เราเรียกมันว่าการทำ **Boxing** นั่นเอง ซึ่งเกิดขึ้นภายในบรรทัดที่ 2

## Unboxing

คราวนี้ตัวแปรที่เราเก็บไว้ใน object เมื่อเราต้องการเอาออกมาใช้งาน ให้กลับมาอยู่ใน Data type ปรกติของมัน เราก็จะต้องทำการ cast มันกลับไปนั่นเองตามโค้ดด้านล่าง

```csharp
int i = 123;      // a value type
object o = i;     // boxing
int j = (int)o;   // unboxing
```

จากโค้ดด้านบน บรรทัดที่ 3 โปรแกรมจะต้องไปเอาค่าที่เก็บในตัวแปร o ออกมา แล้วแปลง data type ให้กลับคืนมาเป็น int นั่นเอง

![](../../../.gitbook/assets/image%20%28504%29.png)

ซึ่งกระบวนการทำ Unboxing นี้อาจจะเกิด error ขึ้นได้ ถ้าข้อมูลที่เก็บอยู่มันไม่สามารถ cast กลับออกมาได้นั่นเอง

