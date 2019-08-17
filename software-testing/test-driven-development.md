---
description: Software Testing
---

# 👦 Test-Driven Development

## 😢 ปัญหา

1. เคยรู้สึกปวดกบาลกันไหม เวลาที่เราเขียนๆงานอยู่แล้ว**เพื่อนมาบอกว่าเจอ bug ในงานของเรา** แล้วพอเราแก้ให้เขาเสร็จ มันก็เดินมาบอกว่า**ไอ้ที่แก้เมื้อกี้มันทำตรงนั้นพังด้วยอ่ะ** ด้วยจิตวิญญาณของโปรแกรเมอร์ของเราเลยต้อง**ตามไปแก้ให้มันต่อ** แล้วพอเราแก้เสร็จ เจอเพื่อนเรามันก็เดินมาบอกว่า อะเค **bug ล่าสุดหายละ แต่ bug ตัวแรกสุดอะกลับมาอีกละ** วนเวียนกันไปเรื่อยๆ 
2. ตอนที่เราเทสกันแต่ละรอบก็ใช้เวลาเทสนานม๊วก เช่น**กว่า developer จะส่งให้ฝั่ง tester ได้เทส** และ**กว่าที่ tester จะส่งผลกลับมาให้ developer ได้** นี่ยังไม่รวมว่าพวก tester จะต้องใช้เวลาทำความเข้าใจว่าจะเทสยังไงด้วยนะ รวมๆแล้ว**เขียนโปรแกรมหรือแก้ bug เสร็จ 1 ครั้ง กว่าจะรู้ผลว่ามี bug หรือเปล่าอาจจะใช้เวลามากกว่า 1 วัน**ก็ได้! 

## 😄 วิธีแก้ปัญหา

ปัญหาที่เกิดขึ้นมันชี้ว่า **โค๊ดที่เราเขียนมันไม่ถูกนำไปเทส** หรือ **เทสที่นำไปทดสอบมันไม่ครอบคลุม** และในบางทีอาจจะหมายถึงเรา**ไม่มีสิ่งที่เรียกว่า Test automation** ก็ได้ทำให้การเทสแต่ละครั้งมันช้าม๊วก ดังนั้นจากที่ว่ามาในเรื่องนี้เราจะมาดูกันว่าการพัฒนาซอฟต์แวร์โดยใช้หลัก **Test-Driven Development** หรือ **TDD** มันจะมาช่วยลดปัญหาที่ว่ามายังไงบ้างกันเน่อ

## 🎥 วีดีโอทั้งหมดของคอร์สนี้

[@Youtube Test-Driven Development \(TDD\)](https://www.youtube.com/playlist?list=PLUjAn8nwWniiL3ToFK8PfmAo8U6IoGAkg)




