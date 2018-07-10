# Aviatrix I1: Destinations

### `knownDestinations`

Remember that all the data about destinations is in `AviatrixData`. We want to have this function return an array like this:

```
["St. Louis", "Phoenix", "Denver", "SLC"]
```

*Can you write the code so that the `knownDestinations` function returns just the keys from that dictionary?*

```swift
func knownDestinations() -> [String] {
    let data = AviatrixData()
    return Array(data.knownDistances.keys)
}
```

Stuck? Remember, to access the data from `AviatrixData`, we have to have an instance of it. Also, look back at the Dictionary slides if you need to refresh on how to access keys.

#### `distance_to`

If you look in `AviatrixData` you'll see that the distances are in there, but how do we get to them?

First, we need to know where we are. The stub starts our plane in St. Louis. So for a first round, let's assume that any distance being calculated is *from* St. Louis.

The distance from St. Louis to Phoenix is 1260 miles. You can see that number inside the `knownDistances` function of `AviatrixData`. We could get to it like this:

```
knownDistances["St. Louis"]!["Phoenix"]!
```

The `knownDistances` variable is a dictionary. `St. Louis` is a key in that dictionary. It points to a value which is *another* dictionary.

`"Phoenix` is a key in that second dictionary. It points to a value 1260, which is what we're looking for.

So the code `knownDistances["St. Louis"]!["Phoenix"]!` gets us the distance between St. Louis and Phoenix. We we look at our `distanceTo` function we have an argument named `target` that is the city we're heading to.

*Write code in your `distanceTo` function that finds the distance between St. Louis and your `target`*. Check the output you see in `main.swift` against the numbers in `AviatrixData`.

```swift
func distanceTo(target : String) -> Int {
    let data = AviatrixData()
    return data.knownDistances["St. Louis"]!["target"]!
}
```

#### Planning for the Future

That'll work great as long as our current location is St. Louis. But we're about to start moving around. How can you modify this line so that it works based on our _current_ location?

```swift
func distanceTo(start: String, target : String) -> Int {
    let data = AviatrixData()
    return data.knownDistances[start]![target]!
}
```

Once this is done, let's update the message in `fly` in `main.swift` that says:

```swift
print("🛬 You've arrived in \(plane.location)!")
```

... so that it actually prints out the planes location.


### Flying

#### Reading `main.swift`

#### `fly_to`

In Aviatrix, find the `flyTo` function. It looks like this:

```
func flyTo(destination : String) {

}
```

The `destination` that comes in is the city like `"Denver"`.
*Can you write one line here that stores that city into the plane's `location` instance variable?*

```swift

class Aviatrix {

    var running = false
    var author : String
    var location : String = "St. Louis"

    // init function, other code

    func flyTo(destination : String) {
        location = destination
    }
}
```

#### Location Update in Gauges

In `main.swift`, there is a `gauges` function that is just printing out some information what the user types in `a`. Uncomment the line that says:

```
print("| Location:  | \(plane.location)")
```

Now, run your program and type in `a`.

## What We've Got

After this work, when you run the program:

* The `planeData` is still mostly blank, but our `Location` is accurate
* Flying to a different city works and we can move city to city
* Refueling doesn't do anything yet

Make sure your code works like that before you move on to [I2: Distances](./i2_distance_and_fuel.markdown).
