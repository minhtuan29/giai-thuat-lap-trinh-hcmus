# Chương 1 : kỹ thuật xử lý lặp
Bài toán 1: viết hàm f(x,n) = x^1/1 + x^2/2 + ... x^n/n  
Giải:
```js

function fraction( numerator, denominator){
    return numerator/denominator;
}


function f(x, range){
    let sum = 0;
  
    let numerator = 1;
    for(let itor = 1; itor <= range; itor++){
      numerator *= x;
      sum += fraction(numerator=numerator, denominator = itor)
    }
  
    console.log(sum);
    return sum;
}


f(x=2, range=5)
```
