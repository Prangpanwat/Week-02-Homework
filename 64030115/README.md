# การบ้าน สัปดาห์ที่ 02

1. สร้าง idf-project ใหม่
![image](https://github.com/Prangpanwat/Week-02-Homework/assets/116150897/40ad8631-f33d-457a-9ee7-51e7ec356b90)

2. สร้าง idf-component ขึ้นใน project ที่สร้างในข้อ 1
![image](https://github.com/Prangpanwat/Week-02-Homework/assets/116150897/20773851-6bb5-4b81-b9a9-aa968b959f04)

3. ทำการ Push project พร้อม component ขึ้นไปที่ remote repository ใน account github ส่วนตัว
![image](https://github.com/Prangpanwat/Week-02-Homework/assets/116150897/2723a85c-1565-4fe8-947c-7a3b926d7f3a)


4. สร้าง idf-project อีก project ที่ไม่เกี่ยวกับในข้อ 1
![image](https://github.com/Prangpanwat/Week-02-Homework/assets/116150897/23ce8a00-a2ef-424f-b2e1-fadad7c74181)

5. เพิ่ม managed component ใน project ในข้อ 4 โดยการเพิ่มไฟล์ idf_component.yml  ในโฟลเดอร์ main จากนั้น build และ run project
![image](https://github.com/Prangpanwat/Week-02-Homework/assets/116150897/a3c09d9e-b429-4c60-8acc-b35d0c9427b2)
![image](https://github.com/Prangpanwat/Week-02-Homework/assets/116150897/fb539d01-3e7b-4fba-b7dd-d90106504a95)

6. เขียน code เพื่อแสดงการใช้งาน component ที่เพิ่มเข้ามาในข้อ 5 แล้ว push โปรเจคไว้บน github
![image](https://github.com/Prangpanwat/Week-02-Homework/assets/116150897/172d2b37-dd37-42a8-8c8e-0347167d4f6c)

```c
#include <stdio.h>
#include <freertos/FreeRTOS.h>
#include <freetos/task.h>
#include "driver/gpio.h"
#include "LED.h"

#define LED_PIN_1 GPIO_NUM_2
#define LED_PIN_2 GPIO_NUM_4
#define LED_PIN_3 GPIO_NUM_5
#define LED_PIN_4 GPIO_NUM_12
#define LED_PIN_5 GPIO_NUM_13
#define LED_PIN_6 GPIO_NUM_14
#define LED_PIN_7 GPIO_NUM_15
#define LED_PIN_8 GPIO_NUM_16

void app_main(void)
{
	LED_init();
    while (1) 
    {
    	LED_toggle(LED_PIN_1);
    	vTaskDelay(1000);
    	
    	LED_toggle(LED_PIN_2);
    	vTaskDelay(1000);
       LED_on(LED_PIN_1);
    }
}

```
## งานที่ต้องส่ง
1. อธิบายการปฏิบัติงานในแต่ละขั้น หรืออาจจะ capture เป็นคลิปแล้ว upload ขึ้น ํYoutube 
2. ส่งงานผ่านการ pull request ใน repo นี้ โดยมีสิ่งที่ต้องส่งคือ  
2.1 คำอธิบายการปฏิบัติงาน และ/หรือ ลิงก์ไปยังคลิปอธิบายการปฏิบัติ  
2.2 link ไปยัง repo ของโปรเจคในข้อ 3 และ 6


## ตัวอย่างไฟล์ idf_component.yml

https://github.com/Special-Topics-Computer-2023/Week-02-Homework/blob/main/example-file-idf_component_yml.md
