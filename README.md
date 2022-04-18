# Giới thiệu
Bài học này viết bằng ngôn ngữ JavaSscript, được xây dựng sao cho bạn đọc có thể hiểu ngay dù không biết JavaScript. Bài học được chia thành các chương được đánh số thứ tự, kéo dài trên trang markdown này. Giải thuật không phải là cấu trúc dữ liệu, nó góp phần làm nên sự khác nhau giữa các cấu trúc dữ liệu, nếu bạn đang học cấu trúc dữ liệu thì nên cài đặt bằng C++ hoặc Java. Bài học này phù hợp cho các bạn đang là sinh viên như mình, đang muốn ôn tập và nghiên cứu. Bài học bắt đầu từ chương 8 trong cuốn Nhập Môn Lập Trình, mình bỏ qua chương 5 giới thiệu về độ phức tạp thuật toán, vì trên mạng đầy rẫy rồi không cần mình viết lại .. Đóng góp nếu bạn thấy hữu ích.  
Dùng ngay IDE JavaScript tại https://onecompiler.com/javascript  
## Chương 8 : kỹ thuật xử lý lặp
1.1 Thuật toán tính tổng hoặc tích số  
Dạng toán : truy hồi <-> tổng quát  
Truy hồi nghĩa là kết quả thứ i sẽ tận dụng lại kết quả thứ i-1, nhằm tránh CPU tính toán lại    
Tổng quát nghĩa là tìm ra công thức tổng quát để tính, không cần truy hồi

Bài toán 1: viết hàm f(x,n) = x^1/1 + x^2/2 + ... x^n/n  
Giải: dùng truy hồi
```js
function phân_số( tử_số, mẫu_số){
    return tử_số/mẫu_số
}


function f(x, hạng){
    let tổng = 0
  
    let bội_dần_đều_truy_hồi = 1
    for(let con_chạy = 1; con_chạy <= hạng; con_chạy++){
      bội_dần_đều_truy_hồi *= x
      tổng += phân_số(tử_số=bội_dần_đều_truy_hồi, mẫu_số=con_chạy)
    }
  
    return tổng
}
```
