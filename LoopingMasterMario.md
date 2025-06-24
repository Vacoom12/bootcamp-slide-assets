# Looping Master Mario

###### By Saksakun Jiarapong, Wanathaphong Kamchoo

---

## What is loop? Why is loop?

---

### What is loop?

**ลูป** คือการทำสิ่งเดิมซ้ำๆ จะสิ้นสุดเมื่อตรงตามเงื่อนไขอะไรบางอย่างที่ถูกกำหนด

**ในทางคอมพิวเตอร์** คือคำสั่งในภาษาโปรแกรมที่ใช้ในการทำชุดคำสั่งเดิมๆ ซ้ำกันหลายๆ ครั้งจนครบกำหนดตามเงื่อนไข

### Loop in real life

ตัวอย่างการวนซ้ำในชีวิตจริง
* ออกกำลังกาย : ออกท่าเดิมซ้ำๆ จนครบตามจำนวนที่ต้องการ
* วิ่งรอบสนาม : วิ่งรอบสนามซ้ำๆ จนครบรอบที่ต้องการ
* นับจำนวน : นับจำนวนคนทั้งหมดในห้องจนครบทุกคน

### Loop in programming

ตัวอย่าง loop ที่มีการใช้ในโปรแกรม/แอพ

**ตีบอสในเกม**

![Boss Fight](https://github.com/Vacoom12/bootcamp-slide-assets/blob/main/Screenshot%202025-06-25%20001134.png?raw=true)

**เล่นเพลย๋ลิสต์เพลง**

![Play Playlist](https://github.com/Vacoom12/bootcamp-slide-assets/blob/main/Screenshot%202025-06-25%20001142.png?raw=true)

---

### What if we don't use loop?

สมมุติว่าอยากเขียน "Hello World~" 30 ครั้ง

```java
public static void main(String[] args) {
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
    System.out.println("Hello World~");
}
```

เทียบกับการใช้ลูป

```java
public static void main(String[] args) {
    for (int i = 0; i < 30; i++) {
        System.out.println("Hello World~");
    }
}
```

### That's why we use loop
    
* ลดความซ้ำซ้อน
* โค้ดสั้นลง กระชับมากขึ้น
* แก้ไขปรับปรุงง่าย
* ประหยัดเวลาในการทำงาน
* อ่านง่ายขึ้นนนน

---

## Coding

---

### How does loop work?

* สร้างตัวแปรมาเพื่อกำหนดการจบลูป
* สร้างเงื่อนไขว่าจะให้จบตอนไหน
* เขียนการทำงานด้านในลูป
* เขียนเงื่อนไขการเปลี่ยนค่าของตัวแปรที่ใช้จบลูป

![Loop Flowchart](https://github.com/Vacoom12/bootcamp-slide-assets/blob/main/Screenshot%202025-06-25%20001147.png?raw=true)

---

### Common loop in programming

* for-loop
* while
* do-while

### While

```java
while (condition) {
    //code
}
```

**Example**

* ต้องมีค่า num มาก่อนถึงจะเช็คเพื่อเข้าลูป

```java
int num = 0;

while (num != 5) {
    System.out.println("Enter number (press 5 to exit): ");
    num = sc.nextInt();
}

System.out.println("End");
```

### Do-While

```java
do {
    //code
} while (condition);
```

**Example**

* ไม่ต้องมีค่า num เริ่มต้น
* ต้องพิมพ์ค่าเข้าไปก่อนอย่างน้อย 1 ครั้ง

```java
int num;

do {
    System.out.println("Enter number (press 5 to exit): ");
    num = sc.nextInt();
} while (num != 5);

System.out.println("End");
```

### For-Loop

```java
for (initialization; condition; iteration) {
    //code
}
```

**Example**

วิ่งรอบสนาม

```java
for (int i = 0; i < 10; i++) {
    System.out.println("วิ่งรอบที่ : " + (i + 1));
}
```

แม่สูตรคูณ

```java
int n = 7;

for (int i = 1; i <= 12; i++) {
    System.out.println(n + " x " + i + " =  " + (n * i));
}
```

### For-Loop vs While vs Do-While

| For-Loop               | While           | Do-While  |
| -------------          | -------------   | ----- |
| รู้รอบที่แน่นอน ในการใช้งาน  | ไม่รู้รอบที่แน่นอน   | ไม่รู้รอบที่แน่นอน |
| สั้น กระชับ               | หากรณีอื่นๆ เช่น True/False        |  หากรณีอื่นๆ เช่น True/False |
| เงื่อนไขบรรทัดเดียว         | update ค่าเพื่อให้ออกลูป       | update ค่าเพื่อให้ออกลูป  |
| นิยมมากที่สุด             |                 | ทำงานก่อน 1 รอบก่อนเช็คเงื่อนไข           | 
|                        |                 | นิยมน้อย           | 

---

### Nested Loop

การเขียนลูปซ้อนในลูป
* เขียนโปรแกรมที่ซับซ้อนมากขึ้น
* พื้นฐานของหลายๆ Algorithm

ลูป i มีลูป j **ซ้อน**อยู่ด้านใน

```java
for (int i = 0; i < 10; i++) {
    for (int j = 0; j < 10; j++) {
        //code
    }
}
```

**Example**

วิ่งรอบสนาม

* i : บอกรอบที่วิ่ง
* j : บอกจำนวนก้าวในรอบที่วิ่ง

```java
int round = 10;
int walk = 20;

for (int i = 0; i < round; i++) {
     for (int j = 0; j < walk; j++) {
        System.out.println("ก้าวที่ " + (j + 1));
    }
    System.out.println("วิ่งครบรอบที่ " + (i + 1));
}
```

แม่สูตรคูณ

* i : เป็นตัวตั้ง
* j : เป็นตัวคูณ

```java
for (int n = 1; n <= 12; n++) {
    for (int i = 1; i <= 12; i++) {
        System.out.println(n + " x " + i + " = " + (n * i));
    }
    System.out.println();
}
```

---

### Pattern

สี่เหลี่ยมจตุรัส N x N

```
* * * * *
* * * * *
* * * * *
* * * * *
* * * * *
```

```java
int N = 5;

for (int i = 1; i <= N; i++) {
    for (int j = 1; j <= N; j++) {
        System.out.print("* ");
    }
    System.out.println();
}
```

พีระมิดชิดซ้าย N ชั้น

```
* 
* * 
* * * 
* * * * 
* * * * *
```

```java
int N = 5;

for (int i = 1; i <= N; i++) {
    for (int j = 1; j <= i; j++) {
        System.out.print("* ");
    }
    System.out.println();
}
```

พีระมิดกลับหัวชิดซ้าย N ชั้น

```
* * * * *
* * * * 
* * * 
* * 
* 
```

```java
int N = 5; 

for (int i = 1; i <= N; i++) {
    for (int j = 1; j <= N - i + 1; j++) {
        System.out.print("* ");
    }
    System.out.println();
}
```

สี่เหลี่ยมข้าวหลามตัดกลับหัว

```
  *
 ***
*****
 ***
  *
```

```java
int n = 3;

for (int i = 1; i <= n; i++) {
    for (int j = 1; j <= n - i; j++) {
        System.out.print(" ");
    }

    for (int k = 1; k <= (2 * i - 1); k++) {
        System.out.print("*"); 
    }
    System.out.println();
}

for (int i = n - 1; i >= 1; i--) {
    for (int j = 1; j <= n - i; j++) {
        System.out.print(" "); 
    }

    for (int k = 1; k <= (2 * i - 1); k++) {
        System.out.print("*"); 
    }
    System.out.println();
}
```

---

### Break

**หยุดลูป**ทั้งหมด**ภายในลูปนั้น**เมื่อตรงเงื่อนไง

```java
while (true) {
    String name = sc.nextLine();

    if (name.equals("")) {
        System.out.println("nueay la");
        break;
      }

    System.out.println("Hi~~~ " + name);
}
```

### Continue

**ข้ามลูป**ไปลูปถัดไป**ภายในลูปนั้น**เมื่อตรงเงื่อนไข

```java
for (int i = 0; i < 100; i++) {
    if (i % 2 == 0) {
        continue;
    }
    System.out.println(i);
}
```

---