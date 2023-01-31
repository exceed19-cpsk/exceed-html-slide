---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
# page transition
transition: fade-out
# use UnoCSS
css: unocss
fonts:
  sans: "Noto Sans Thai, Noto Sans"
  serif: "Noto Serif Thai"
  mono: "Fira Code"
---

# HTML + CSS

มาเรียน HTML กับ CSS กันดีกว่า

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: slide-left
---

# HTML คืออะไร

HTML เป็นภาษาที่หลักที่ใช้ในการเขียนเว็บ หน้าที่ของ HTML คือการบอกว่าส่วนไหนของเว็บคืออะไร
รวมถึงการจัดเนื้อหาต่าง ๆ เช่น รูปภาพ วิดีโอ หรือลิงก์

HTML ย่อมาจาก HyperText Markup Language

## ตัวอย่าง HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Exceed Impact</title>
  </head>
  <body>
    <h1>Hello, World</h1>
  </body>
</html>
```


<!--
อันนี้ให้สอนตาม slide ได้เลย
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
Here is another comment.
-->

---
transition: slide-left
---

# ส่วนประกอบของ HTML

HTML ประกอบด้วย tag เช่น `html`, `body`, `h1` แต่ละ tag จะครอบด้วยเครื่องหมาย `<>` และปิดด้วย `</>`
เช่น `<h1>Hello, World</h1>` จะเป็น tag `h1` ที่มีข้อความ `Hello, World` อยู่ด้านใน

สำหรับบาง tag จะมี attribute ที่สามารถใส่เข้าไปได้ เช่น `a` เป็น tag ที่ใช้แสดงลิงก์ไปหน้าอื่น ๆ
จะใส่ `href` เพื่อบอกว่าไปไหน ส่วนข้อความด้านใน tag จะเป็นข้อความที่แสดงขึ้นมา

```html
<a href="https://www.youtube.com/watch?v=mW61VTLhNjQ?autoplay=1" target="_blank">Totally not a rickroll</a>
```

<a href="https://www.youtube.com/watch?v=mW61VTLhNjQ?autoplay=1" target="_blank">Totally not a rickroll</a>


---
transition: slide-left
---

# ส่วนประกอบของไฟล์ HTML

ในไฟล์ HTML ปกติจะแบ่งออกเป็น
- Doctype ที่จะบอก version ของตัว HTML (ควรใส่)
- Head จะบอก title (ชื่อหน้าเว็บ), รวม CSS กับ JavaScript, รวมถึง metadata อย่างเช่น description ของตัวเว็บ
  ส่วนนี้จำสำคัญเวลาทำ SEO (ทำให้เว็บขึ้น Google) และก็แชร์ social media
- Body แสดงหน้าเว็บและอาจจะมี script เพิ่มเติมที่ไม่ได้อยู่ใน head

ทั้งไฟล์ HTML จะถูกครอบด้วย tag `html`

เรื่อง JavaScript จะพูดกันในวันหน้า ๆ นะครับ

---
transition: slide-left
---

# ตัวอย่างไฟล์ HTML

```html {all|2-6|7-12}
<html>
  <head>
    <title>Hutao's Workshop</title>
    <link rel="stylesheet" href="index.css" >
    <script src="index.js" />
  </head>
  <body>
    <main>
      <h1>Hutao's Workshop</h1>
      <p>Hutao is the best girl in Genshin Impact.</p>
    </main>
  </body>
</html>
```


---

# Tag สำคัญ ๆ

- `a` เป็น tag สำหรับใส่ link ไปหน้าอื่น ๆ
- `img` เป็น tag สำหรับใส่รูปภาพ
- `div` เป็น tag ที่ใช้ในการจัดหน้าโดยใช้ CSS ใน HTML5 จะมี tag ที่ใส่แบบเดียวกัน เช่น `section`, `aside` แต่ว่าไม่จำเป็นต้องใช้ใน lab นี้
- `link` เป็น tag สำหรับใส่ CSS ในหน้า (การใช้งานแบบอื่นสามารถศึกษาด้วยตนเอง)
- `h1` ถึง `h6` สำหรับใส่หัวข้อเรื่อง
- `p` สำหรับใส่ข้อความเป็น **p**aragraph


<!--
เตรียมทำแลป
-->


---
layout: section
---
# Lab Time!

<!-- lab 1: Basic HTML -->

---
transition: slide-left
---
# Tag สำคัญ (ต่อ)

<div grid="~ cols-2 gap-4">

<div>

- `ul` และ `ol` จะเป็น tag สำหรับการทำ list ทั้งคู่ โดย `ul` จะไม่เรียงลำดับ แต่ `ol` จะเรียงลำดับ
- `li` จะเป็น tag สำหรับแต่ละรายการของ list

```html
<h2>Important topics</h2>
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>Genshin Impact</li>
</ul>
```
</div>
<div>
  <h2>Important Topics</h2>
  <ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>Genshin Impact</li>
  </ul>
</div>
</div>

---
transition: slide-left
---
# Form

หน้าเว็บยังไงก็ต้องมีการกรอกข้อมูล ดังนั้น tag ที่เกี่ยวกับฟอร์มจะสำคัญมาก ๆ
- `form` เป็นการบอกว่าส่วนที่จะอยู่ตรงนี้เป็น form ที่ให้กรอก ถ้าต่อกับ backend จะสามารถ
  ส่งข้อมูลไปยัง backend ได้ผ่าน HTTP request
- `input` เป็น tag สำหรับรับข้อมูลเป็นรูปแบบต่าง ๆ กำหนดโดย attribute ชื่อว่า `type`
- `label` เป็น tag สำหรับบ่งบอกว่า `input` แต่ละอันหมายความว่าอะไร
- `button` เป็น tag สำหรับปุ่ม ปกติจะไม่ค่อยได้ใช้เวลาเขียน HTML ร่วมกับ backend ทั่วไป แต่จะใช้บ่อยเวลาทำ React
- `textarea` เป็น tag ข้อความยาว
- `select` และ `option` ตัวเลือก



---
transition: slide-left
---

# ตัวอย่าง Form HTML

```html
<form action="/register.php" method="POST">
  <label for="name">Name</label>
  <input id="name" name="name" />
  <label for="surname">Surname</label>
  <input id="surname" name="surname" />
</form>
```

---


# ตาราง

ในบางงานอาจจะต้องใช้ตารางในการแสดงผล HTML เลยมี tag สำหรับตารางโดยเฉพาะ

- `table` คือตัวตารางเลย
- `thead` = หัว `tbody` = ตัว `tfoot` = ท้าย
- `tr` หมายถึงแถวหนึ่งแถว
- `td` คือข้อมูลในตาราง `th` จะคล้าย ๆ `td` แต่ใช้กับตาราง


---

# Code

```html
 <table>
  <thead>
    <tr>
      <th>Month</th>
      <th>Savings</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>$100</td>
    </tr>
    <tr>
      <td>February</td>
      <td>$80</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Sum</td>
      <td>$180</td>
    </tr>
  </tfoot>
</table>
```

---

# ตารางที่ได้

 <table>
  <thead>
    <tr>
      <th>Month</th>
      <th>Savings</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>$100</td>
    </tr>
    <tr>
      <td>February</td>
      <td>$80</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Sum</td>
      <td>$180</td>
    </tr>
  </tfoot>
</table>

---

# Self-study (Optional)

- [https://developer.mozilla.org/en-US/docs/Learn/HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML)
  เป็นลิงก์ของ MDN พี่ใช้ประจำเวลาจำ syntax ไม่ได้ นอกจาก HTML แล้วก็มีเรื่อง web อื่น ๆ อีก
- [https://www.freecodecamp.org/learn/](https://www.freecodecamp.org/learn/)
  เป็นเว็บที่มีบทความและคอร์สเรียนฟรี ๆ ตั้งแต่ HTML, CSS, JavaScript หรือแม้กระทั่งสาย Data


---
layout: center
---

# Next Section

Section ถัดไปจะพูดถึง CSS โดยละเอียด การสอน CSS จะเป็นแบบให้ทำแลป จะไม่ได้มี slide แล้วนะครับ
