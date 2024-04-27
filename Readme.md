# Single Phase High Performance Wide Span Energy Metering IC (單向meter)
Application 應用
===
#### M90E26被用於單相兩線（1P2W）、單相三線（1P3W）或防篡改電能表的有功和無功量測。透過其量測功能，M90E26還可以用於需要測量電壓、電流等的功率儀器。

Interface 介面
===
#### M90E26支援Serial Peripheral Interface (SPI)和UART接口。接口的選擇由USEL引腳控制。當USEL引腳為低電平時，選擇SPI接口。當USEL引腳為高電平時，選擇UART接口。請注意，在重置後USEL引腳不應該改變。

SPI Interface
---
#### SPI是一種全雙工、同步的通道。SPI有兩種模式：四線模式和三線模式。在四線模式中，使用四個引腳：$\bar{CS}$、SCLK、SDI和SDO。在三線模式中，使用三個引腳：SCLK、SDI和SDO。SDI上的數據在SCLK的上升沿時被移入芯片中，而SDO上的數據在SCLK的下降沿時從芯片中移出。LastData寄存器（地址06H）存儲最近讀取或寫入的16位數據。
FOUR-WIRE MODE
---
#### 在四線模式下，CS引腳必須在整個讀取或寫入操作期間保持低電平。SDI上的第一個位定義了訪問類型，而低7位被解碼為地址。  
>註: 讀取模式第一位為 1 (HIGH)，寫入模式則是 0 (LOW)     
------------------------
### Read Sequence  
![read-mode](uploads/ac2a42fb08c6d1174d255656f755e1a8/read-mode.PNG)  
### Write Sequence  
![write-mode](uploads/4c113a8a3729b414e152c671a0dd05d5/write-mode.PNG)
