# Single Phase High Performance Wide Span Energy Metering IC (單向 meter)

# Application 應用

#### M90E26 被用於單相兩線（1P2W）、單相三線（1P3W）或防篡改電能表的有功和無功量測。透過其量測功能，M90E26 還可以用於需要測量電壓、電流等的功率儀器。

# Interface 介面

M90E26 支援 Serial Peripheral Interface (SPI)和 UART 接口。接口的選擇由 USEL 引腳控制。當 USEL 引腳為低電平時，選擇 SPI 接口。當 USEL 引腳為高電平時，選擇 UART 接口。請注意，在重置後 USEL 引腳不應該改變。

## SPI Interface

#### SPI 是一種全雙工、同步的通道。SPI 有兩種模式：四線模式和三線模式。在四線模式中，使用四個引腳：$\bar{CS}$、SCLK、SDI 和 SDO。在三線模式中，使用三個引腳：SCLK、SDI 和 SDO。SDI 上的數據在 SCLK 的上升沿時被移入芯片中，而 SDO 上的數據在 SCLK 的下降沿時從芯片中移出。LastData 寄存器（地址 06H）存儲最近讀取或寫入的 16 位數據。
