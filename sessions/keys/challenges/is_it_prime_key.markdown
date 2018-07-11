```swift4
func isItPrime(num: Int) -> Bool {
    if num == 1 {
        return false
    } else if num == 2 {
        return true
    } else {
        for current in 2..<num {
            if num % current == 0 {
                return false
            }
        }
        return true
    }
}

let answer = isItPrime(num: 13)
print(answer)
```
