# Huỳnh Tấn Phát
### BÁO CÁO HỌC CON TRỎ
[I. Địa chỉ](#Địa chỉ)  
[1. Các khái niệm liên quan đến biến](#Các khái niệm liên quan đến biến)  
[2. Địa chỉ của biến](#Địa chỉ của biến)  
[II. Con Trỏ](#Con Trỏ)  
[1. Khái niệm con trỏ](#Khái niệm con trỏ)  
[2. Phân loại con trỏ](#Phân loại con trỏ)
[3. Khai báo biến con trỏ](#Khai báo biến con trỏ)  
[4. Con trỏ với mảng một chiều và với mảng nhiều chiều](#Con trỏ với mảng một chiều và với mảng nhiều chiều)  
[5. Các phép toán trên con trỏ](#Các phép toán trên con trỏ)  
[III. QUY TẮC SỬ DỤNG CON TRỎ TRONG CÁC BIỂU THỨC](#QUY TẮC SỬ DỤNG CON TRỎ TRONG CÁC BIỂU THỨC)  
[1. Tên con trỏ](#Tên con trỏ)  
[2. Dạng khai báo của con trỏ](#Dạng khai báo của con trỏ)  
[IV.QUY TẮC VỀ KIỂU GIÁ TRỊ TRONG KHAI BÁO](#QUY TẮC VỀ KIỂU GIÁ TRỊ TRONG KHAI BÁO)  
[V. BỘ ĐỊNH TÍNH CONST VỚI CON TRỎ](#BỘ ĐỊNH TÍNH CONST VỚI CON TRỎ)  

<a name="Địa chỉ">
##I. Địa chỉ:  
Dựa vào kiểu dữ liệu khi khai báo biến máy sẽ `cấp phát` cho biến một địa chỉ để lưu trữ biến đó trên vùng nhớ. Mỗi biến có `kiểu khác nhau` thì được `lưu vào các địa chỉ khác nhau`.

<a name="Các khái niệm liên quan đến biến">
##1. Các khái niệm liên quan đến biến:  
*Tên biến  
*Kiểu biến  
*Gía trị của biến  
`Ví dụ: int us = 5; -> int: kiểu biến; us: tên biến; 5: giá trị của biến`

<a name="Địa chỉ của biến">
##2. Địa chỉ của biến:  
<li>Khái niệm:  
Địa chỉ của biến là số thứ tự của byte đầu tiên trong một dãy các byte liên tiếp mà máy dành cho biến.
<li>Phân loại địa chỉ của biến:  
+Địa chỉ kiểu int: hai biến kiểu int liên tiếp cách nhau 2 byte  
+Địa chỉ kiểu float: hai biến kiểu float liên tiếp cách nhau 4 byte  
+Địa chỉ kiểu double,struct, user defined type v.v...
<li>Phép lấy địa chỉ của một biến: Phép toán **`&x`** cho ta địa chỉ của biến x  

<a name="Con Trỏ">
##II. Con Trỏ:

<a name="Khái niệm con trỏ">
##1. Khái niệm con trỏ:  
Con trỏ là một biến dùng để chứa địa chỉ. Mỗi loại địa chỉ thì có một loại con trỏ tương ứng. Trước khi sử dụng con trỏ ta phải khai báo trước khi sử dụng.  

<a name="Phân loại con trỏ">
##2. Phân loại con trỏ:  
<li>Con trỏ kiểu int dùng để chứa địa chỉ các biến kiểu int.  
<li>Con trỏ kiểu float dùng để chứa địa chỉ các biến kiểu float.  
<li>Con trỏ kiểu double dùng để chứa địa chỉ các biến kiểu double.  

<a name="Khai báo biến con trỏ">
##3. Khai báo biến con trỏ:  
`<Kiểu_dữ_liệu>*<tên_biến_con_trỏ>`  
Ví dụ: int `*p,*a;`  

<a name="Con trỏ với mảng một chiều và với mảng nhiều chiều">
##4. Con trỏ với mảng một chiều và với mảng nhiều chiều:  
`Con trỏ cũng là một biến, do đó nó có thể được lưu trữ trong các mảng. Mảng này được gọi là mảng con trỏ`
a. Con trỏ với mảng một chiều:
Các phần tử của mảng có thể được xác định thông qua con trỏ.
Ta có khai báo : float a[10];
Ta có tên mảng chính là một hằng địa chỉ trỏ tới địa chỉ phần tử đầu tiên của mảng và
```sh
    a <=> &a[0]  
    a+i <=> &a[i]  
    *(a+i) <=> a[i]  
```
b. Con trỏ với mảng nhiều chiều:  
Bộ nhớ lưu mảng 2 chiều giống như mảng 1 chiều. Vì vậy ta hoàn toàn có thể biểu diễn mảng 2 chiều bằng con trỏ giống như mảng 1 chiều.   
ví dụ: Tạo một mảng 2 chiều có kích thước m x n
````sh
int m = 10, n = 5;
int **Pointer_Array = new int*[m];
 
for (int i = 0; i < m; i++)
{
	Pointer_Array[i] = new int[n];
}
```

<a name="Các phép toán trên con trỏ">
##5. Các phép toán trên con trỏ:  
<li> Phép gán: Chỉ thực hiện khi cùng kiểu. Khi sử dụng cần phải dùng phép ép kiểu.  
`ví dụ: int x; char *p; p=(char*)(&x);`  
<li> Phép tăng giảm địa chỉ:  
<li> Phép so sánh: dùng để so sánh các con trỏ cùng kiểu  

<a name="QUY TẮC SỬ DỤNG CON TRỎ TRONG CÁC BIỂU THỨC">
##III. QUY TẮC SỬ DỤNG CON TRỎ TRONG CÁC BIỂU THỨC

<a name="Tên con trỏ">
##1. Tên con trỏ:  
Sử dụng địa chỉ chứa trong con trỏ.  
Ví dụ: `float a,*p; p=&a;`

<a name="Dạng khai báo của con trỏ">
##2. Dạng khai báo của con trỏ :  
Sử dụng giá trị lưu tại vùng nhớ mà con trỏ trỏ tới.  
Ví dụ:
```sh
 float x=5,y,z=20,*px,*pz;  
 px=&x; // khi đó *px = x =5  
 pz=&z; // *py=y=10  
```

Kết luận: px, pz có kiểu là con trỏ float thì px,pz thuộc kiểu số thực.

<a name="QUY TẮC VỀ KIỂU GIÁ TRỊ TRONG KHAI BÁO">
##IV.QUY TẮC VỀ KIỂU GIÁ TRỊ TRONG KHAI BÁO:  

Mọi thành phần của cùng một khai báo khi xuất hiện trong biểu thức đều cho cùng một kiểu giá trị.  

<a name="BỘ ĐỊNH TÍNH CONST VỚI CON TRỎ">
##V. BỘ ĐỊNH TÍNH CONST VỚI CON TRỎ:

- Dùng để khai báo và khởi đầu giá trị trong các biến trong mà sau này giá trị của nó không cho phép thay đổi bởi các lệnh trong chương trình. Chúng được gọi là đối tượng hằng.  
- Dùng để khai báo các đối con trỏ mà trong thân hàm ta không được phép làm thay đổi  giá trị của các đối tượng được trỏ bởi các đối này.  
