```swift4
func leapYear(year: Int) -> Bool {

    if year % 400 == 0 {
        return true
    } else if (year % 4 == 00) && (year % 100 != 0) {
        return true
    }
    return false
}

let answer = leapYear(year: 2100)
print(answer)
```x
