QQ 填充算法和Tea加解密的golang实现
=========
Example:
```go
  package main

  import (
    "log"
    "github.com/sun8911879/qqtea"
  )

  func main() {
    key := []byte{120, 76, 249, 219, 21, 206, 98, 255, 135, 49, 196, 249, 195, 140, 250, 13}
    value := []byte{0, 3, 31, 3, 90, 125, 0, 0, 0, 5, 0, 0, 0, 16, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 224, 243, 85, 220, 6, 100, 0, 0, 0, 0, 1, 66, 151, 244, 75, 19, 149, 82, 53, 36, 91, 36, 151, 57, 157, 122, 147, 41, 35, 190, 132, 225, 108, 214, 174, 82, 144, 73, 241, 241, 187, 233, 235, 0, 0, 0, 0, 1, 70, 96, 30, 211, 198, 36, 22, 191, 202, 162, 158, 158, 184, 154, 210, 78, 32, 2, 149, 246, 0, 0, 0, 1, 0, 0}
    t,err := tea.NewCipher(key)
    if err != nil{
      return err
    }
    result := t.Encrypt(value)
    log.Println(result)
    result = t.Decrypt(result)
    log.Println(result)
  }
```


> golang 算法根据 [QQ填充算法和TEA 加解密的JavaScript实现](https://github.com/xqin/qqtea) 改写而成.
>
  
