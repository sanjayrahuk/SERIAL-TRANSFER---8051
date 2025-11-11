# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**

#include<reg51.h> void main(void)

{

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

while(1)

{ SBUF='A';

while(TI==0); TI=0;

}

}

**(ii)	Serial port to Transfer a Message**

#include<reg51.h> void main(void)

{

unsigned char msg[]="Programming 8051"; unsigned char i;

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

for (i=0; i<17;i++)

{

SBUF= msg[i]; while(TI==0); TI=0;

}

while(1);

}

 
**OUTPUT:**
<img width="1919" height="1174" alt="Screenshot 2025-11-11 083529" src="https://github.com/user-attachments/assets/e018d502-b42b-4807-9663-5d34816df6e6" />

<img width="1919" height="1150" alt="Screenshot 2025-11-11 083303" src="https://github.com/user-attachments/assets/eae39b09-e307-4809-a3b6-3c0fa88dd793" />


**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
