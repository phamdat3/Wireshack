# Tìm hiểu về Wireshark & Tshark
Thực hiện : **Phạm Đạt**
---
 
# Mục lục

[1. Wireshark](#1)

	[ 1.1 Filter]( #1.1)

	[ 1.2 Phân tích gói tin]( #1.2)

[2. Tshark](#2)

	[ 2.1 Filter]( #2.1)

	[ 2.2 Phân tích gói tin]( #2.2)


---

# Nội dung

<a name="1"></a>
## 1. Wireshark

<a name="1.1"></a>
	### 1.1 Filter
**Một số filter thường dùng:**
- Chú ý một số toán tử được dùng trong câu lệnh:
	```
	eq | == : Equal
	ne | != : Not Equal
	gt | >  : Greater Than
	lt | <  : Less Than
	ge | >= : Greater than or Equal to
	&&      : And(và)
	||      : Or (hoặc)
	!		: Not(phủ định)
	 ```
- Protocol: 
	- Gõ thẳng: tcp, udp, http....
	- Hay mạnh mẽ hơn khi tao biết được port cảu gói tin đó thì có thể kết hợp cả port và protocol:
	`tcp.port == 25` hoặc `tcp.port eq 25`
- Địa chỉ ip:
	- `ip.src == 216.58.220.196` : Lọc các gói tin có địa chỉ sourece là 216.58.220.196
	- `ip.dst == 192.168.2.119`  : Lọc các gói tin có địa chỉ distination là 192.168.2.119
	- `ip.addr == 192.168.2.119` : Lọc các ogis tin có địa chỉ là 192.168.2.119 (bao gồm cả souce và destination)
- Chiều dài gói tin:
	Khi ta muốn lọc những gói tin có 1 chiều dài nhất định: `frame.len == 54`

- Follow Stream: Để xem rõ một phiên trao đổi các gói tin của server và client
vd: `tcp.stream eq 3`
<img src="https://imgur.com/ilmktBX">

<a name="1"></a>
	## 2.1 Phân tích gói tin







<a name="2"></a>
## 2. Tshark

<a name="2.1"></a>
	## 2.1 Filter
Một số **filter** thường dùng
- 

<a name="2.2"></a>
	## 2.2 Phân tích gói tin





