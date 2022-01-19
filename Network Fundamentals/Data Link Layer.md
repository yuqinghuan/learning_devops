# 数据链路层
## 职责
交换通过物理层传输的 frame

数据链路层从网络层接收数据包并处理提供 hop to hop 通信或通过物理链路直接连接的实体之间的通信。

换句话说，它使通过物理链路进行可理解的通信成为可能，该链路仅在两个直接连接的主机之间传输 0 和 1。

## 类型

### point-to-point data link layer
### Local Area Networks(LAN)
[参考](https://en.wikipedia.org/wiki/Computer_network)
end-systems and routers

### Non-Broadcast Multi-Access (NBMA)
ATM, Frame Relay and X.2


## 传输解决方案(分片机制)

### Idle Physical Layer

### Multi-symbol Encodings

### Stuffing
* Bit stuffing
    
    01111110

    it sends all the bits of the frame and inserts an additional bit set to 0 after each sequence of five consecutive 1 bits
* Character stuffing

    DLE STX is used to mark the beginning of a frame, and DLE ETX is used to mark the end of a frame.
    DLE 用于转义

## 错误处理
### 奇偶校验(Parity Bit)
当交换 7 位字符时，通常使用奇偶校验方案。 在这种情况下，第八位通常是奇偶校验位。
可以检测出奇数位错误的 帧
### 三重模块化冗余(Triple Modular Redundancy)
To transmit a bit set to 1, the sender transmits 111 and to transmit a bit set to 0, the sender transmits 000

[汉明码](https://en.wikipedia.org/wiki/Hamming_code)
