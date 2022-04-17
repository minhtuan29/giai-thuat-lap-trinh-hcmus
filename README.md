# Chương 1 : kỹ thuật xử lý lặp
Bài toán 1: viết hàm f(x,n) = x^1/1 + x^2/2 + ... x^n/n  
Giải:
```js
function phân_số( tử_số, mẫu_số){
    return tử_số/mẫu_số
}


function f(x, hạng_cuối){
    let tổng = 0
  
    let bội_dần_đều = 1
    for(let con_chạy = 1; con_chạy <= hạng_cuối; con_chạy++){
      bội_dần_đều *= x
      tổng += phân_số(tử_số=bội_dần_đều, mẫu_số=con_chạy)
    }
  
    return tổng
}
```

```python

def phân_số(tử, mẫu):
  return tử/mẫu

def f(x, hạng_cuối):
  tổng = 0
  
  bội_dần_đều = 1
  for con_chạy in range(1, hạng_cuối+1):
    bội_dần_đều *= x
    tổng += phân_số(tử=bội_dần_đều, mẫu=con_chạy)
    
  return tổng
```
