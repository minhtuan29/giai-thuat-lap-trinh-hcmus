# Chương 1 : kỹ thuật xử lý lặp
Dạng toán : truy hồi <-> tổng quát  
Truy hồi nghĩa là kết quả thứ i sẽ tận dụng lại kết quả thứ i-1  
Tổng quát nghĩa là tìm ra công thức tổng quát để tính, không cần truy hồi

Bài toán 1: viết hàm f(x,n) = x^1/1 + x^2/2 + ... x^n/n  
Giải: dùng truy hồi
```js
function phân_số( tử_số, mẫu_số){
    return tử_số/mẫu_số
}


function f(x, hạng_cuối){
    let tổng = 0
  
    let bội_dần_đều_truy_hồi = 1
    for(let con_chạy = 1; con_chạy <= hạng_cuối; con_chạy++){
      bội_dần_đều_truy_hồi *= x
      tổng += phân_số(tử_số=bội_dần_đều_truy_hồi, mẫu_số=con_chạy)
    }
  
    return tổng
}
```
