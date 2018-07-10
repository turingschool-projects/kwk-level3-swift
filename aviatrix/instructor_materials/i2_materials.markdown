# Aviatrix I2: Distance & Fuel

### In The Simulator

### `distanceTraveled`

In Aviatrix, we need to create a `distanceTraveled` instance variable -- it's just a number that's stored, not a method that does calculations. We need to set it to `0` when the plane is first created.

```swift
class Aviatrix {

    var running = false
    var author : String
    var location : String = "St. Louis"
    var distanceTraveled : Int = 0

    //other code
}
```

But it never gets changed. What code can you add to the `flyTo` function so that it updates the value of `distanceTraveled`?

```swift
func flyTo(destination : String) {
    let data = AviatrixData()
    distanceTraveled += data.knownDistances[location]![destination]!

    location = destination
}
```

## Burning Fuel

### In The Console vs. Code

### Max Fuel

*Can you modify the code in your Aviatrix so the Max Fuel shows up as 5000 gallons?* Think back to what we did to get `distanceTraveled` to appear.


```swift
class Aviatrix {

    var running = false
    var author : String
    var location : String = "St. Louis"
    var distanceTraveled : Int = 0
    var maxFuel : Double = 5000.0
}
```

INSTRUCTOR: `maxFuel` could also be an Integer; the students will just have to do another conversion later. One way isn't better than the other; just different! Just an FYI.

### Fuel to Fly

Let's add another instance variable - `milesPerGallon` and set it to `0.4`.

*Can you modify your `flyTo` in the `Aviatrix` class method so that it calculates how much fuel is used during the flight and decreases `fuelLevel` the right amount?*

```swift
class Aviatrix {

    var running = false
    var author : String
    var location : String = "St. Louis"
    var distanceTraveled : Int = 0
    var maxFuel : Double = 5000.0
    var milesPerGallon = 0.4

    // init function, other code

    func flyTo(destination : String) {
      let data = AviatrixData()
      distanceTraveled += data.knownDistances[location]![destination]!
      location = destination

      let usedFuel = Double(distanceTraveled) * milesPerGallon
      fuelLevel -= usedFuel
    }
}
```

## Refueling

### In The Simulator

### `refuel` - Iteration 0

### `refuel` - First Try

Let's create an instance variable that starts the `fuelLevel` at `5000.0`.

First there's a call to the `refuel` function. Find that function in your Aviatrix.

*Can you write one line of code that fills the gas tank back to it's maximum level?*

```swift
class Aviatrix {
  var running = false
  var author : String
  var location : String = "St. Louis"
  var distanceTraveled : Int = 0
  var maxFuel : Double = 5000.0
  var milesPerGallon = 0.4
  var fuelLevel : Double = 5000.0

  func refuel() {
      fuelLevel = 5000.0
  }
}
```

### `refuel` - Doing Better

*First: return a Double out of this function.*
*Second: Can you improve your `refuel` method so that these three values are correctly calculated?*

```swift
func refuel() -> Double {
    let data = AviatrixData()
    let fuelNeeded = maxFuel - fuelLevel
    let fuelPrice = data.fuelPrices[location]
    fuelLevel = 5000.0
    return fuelNeeded
}
```

NOTE: There are other ways to solve this, not all solutions will look the same, that's ok! As long as it does it's job 🤓

### Tracking Total Fuel Costs

Create a `fuelCost` variable in `Aviatrix` that starts at zero. Each time you refuel, add the amount that you spent to the total `fuelCost`. Read your gauges after two refuels and make sure that the total is correct.

```swift
class Aviatrix {
  var running = false
  var author : String
  var location : String = "St. Louis"
  var distanceTraveled : Int = 0
  var maxFuel : Double = 5000.0
  var milesPerGallon = 0.4
  var fuelLevel : Double = 5000.0
  var fuelCost: Double = 0.0

  // other code

  func refuel() -> Double {
    let data = AviatrixData()
    let fuelNeeded = maxFuel - fuelLevel
    let fuelPrice = data.fuelPrices[location]
    let cost = fuelNeeded * fuelPrice!
    fuelCost += cost
    fuelLevel = 5000.0
    return fuelNeeded
  }

}
```
