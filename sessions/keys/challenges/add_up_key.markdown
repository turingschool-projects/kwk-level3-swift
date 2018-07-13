# Add Up 

```swift
func addUp(num: Int) -> Int {
  var sum = 0

  for current in 0...num {
    sum += current
  }  

  return sum
}

print(addUp(num: 4))
```
