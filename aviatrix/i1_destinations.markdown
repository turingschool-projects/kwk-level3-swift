# Aviatrix I1: Destinations

As you can see in the `main.swift`, our plane should be able to fly places. But all it can do is stay on the runway in St. Louis. Let's build up the functionality to move between cities.

## What We're Going For

When this iteration is done we should be able to fly between known cities. When we run the program and hit `b` to fly we will see some output like this:

```
Where would you like to fly to?

0) St. Louis (0 miles)
1) Phoenix (1260 miles)
2) Denver (768 miles)
3) Salt Lake City (1150 miles)

Destination Number:
```

## The Data

Open the `AviatrixData` file and check out the data that's in there. You should find:

* `fuelPrices` in a later iteration we'll work on purchasing fuel. At that time we'll need this collection of fuel prices.
* `knownDistances` is a huge dictionary that defines the distances between the supported cities where each city marker points to another dictionary. The second-level dictionary has the cities you could fly to along with the distance to get there.

## Building the Menu

Right now when we enter `b` for the fly menu we just see:

```
Action: b

Where would you like to fly to?

0) St. Louis (0 miles)
```

Let's work on displaying more destinations.

### Looking at the Simulator

The `fly` method in the simulator is what's outputting this menu. It's some of the more complicated code in the simulator file, but we can pick it apart piece by piece.

On the third line of the `fly` function we can see it's calling `plane.knownDestinations` and iterating over that array. We need to modify the `knownDestinations` function.

### `known_destinations`

Remember that all the data about destinations is in `AviatrixData`. We want to have this function return an array like this:

```
["St. Louis", "Phoenix", "Denver", "SLC"]
```

*Can you write the code so that the `known_destinations` method returns just the keys from that dictionary?*

Run your code in the simulator and you should see output like this:

```
Action: b

Where would you like to fly to?

0) St. Louis (0 miles)
1) St. Louis (0 miles)
2) St. Louis (0 miles)
3) St. Louis (0 miles)
```

St. Louis shows up four times instead of one. That's progress.

### `name_for`

If you go back to the simulator code, look for the line of code that has `plane.name_for(marker)`. It's taking a marker like `:denver` and trying to turn it into `"Denver"`.

Find the `name_for` method in your code. It looks like this:

```
def name_for(location_marker)
  "St. Louis" #stub
end
```

The `location_marker` that's getting passed in is the same as the key in our `location_names` dictionary. Change this method so it's returning the value that is attached to that key.

#### Results

If you get that method right and run the simulator, you'll get output like this:

```
Action: b

Where would you like to fly to?

0) St. Louis (0 miles)
1)  (0 miles)
2)  (0 miles)
3)  (0 miles)
```

Since the other cities aren't in our dictionary, they are nil, so nothing shows up. Let's make sure our `location_names` function returns the location names dictionary which is in our `AviatrixData` file.

```
Action: b

Where would you like to fly to?

0) St. Louis (0 miles)
1) Phoenix (0 miles)
2) Denver (0 miles)
3) Salt Lake City (0 miles)
```

We've got the city names and next want to add in the distances.

### Distance to Destination

In the simulator we can find the line that outputs that distance. It relies on the variable `distance` that was created here:

```
distance = plane.distanceTo(target : String)
```

So to get the distance to display correctly we've got to look at the `distanceTo` function in our code.

#### `distance_to`

If you look in `AviatrixData` you'll see that the distances are in there, but how do we get to them?

First, we need to know where we are. The stub starts our plane in St. Louis. So for a first round, let's assume that any distance being calculated is *from* St. Louis.

The distance from St. Louis to Phoenix is 1260 miles. You can see that number inside the `knownDistances` method of `AviatrixData`. We could get to it like this:

```
knownDistances["St. Louis"]!["Phoenix"]!
```

The `knownDistances` variable is a dictionary. `"St. Louis` is a key in that dictionary. It points to a value which is *another* dictionary.

`"Phoenix` is a key in that second dictionary. It points to a value 1260, which is what we're looking for.

So the code `knownDistances["St. Louis"]!["Phoenix"]!` gets us the distance between St. Louis and Phoenix. We we look at our `distanceTo` function we have an argument named `target` that is the city we're heading to.

*Write code in your `distanceTo` function that finds the distance between St. Louis and your `target`*. Check the output you see in `main.swift` against the numbers in `AviatrixData`.

#### Planning for the Future

You probably ended up with a line of code that looked like this:

```
return data.knownDistances["St. Louis"]![target]!
```

That'll work great as long as our current location is St. Louis. But we're about to start moving around. How can you modify this line so that it works based on our _current_ location?

#### Results

When you've got it right and run your simulator, your fly menu will look like this:

```
Action: b

Where would you like to fly to?

0) St. Louis (0 miles)
1) Phoenix (1260 miles)
2) Denver (768 miles)
3) Salt Lake City (1150 miles)
```

Try flying to Denver -- you'll get this message: "🛬 You've arrived in St. Louis!" Hmm... I thought we just flew to Denver? Looks like we have some more work to do.

### Flying

We're displaying the menu of destinations. We're allowing the user to pick a destination. But our plane isn't moving.

#### Reading the Simulator

Back in `main.swift` look at the `fly` function (inside the 'if' statement). You'll find some lines that looks like this:

```
desiredLocation = plane.knownDestinations()[response!]
...

plane.flyTo(destination: desiredLocation)
```

Let's break that down:

* The `response` here is the menu option number that the user typed in, like `2` for Denver
* `knownDestinations` is an array that came from the `known_destinations` method we wrote earlier. So `destinations` contains the array `["St. Louis", "Phoenix", "Denver", "SLC"]`
* `knownDestinations()[response!]` when the `number` is `2` is like `knownDestinations[2]` which picks out the marker `"Denver"`
* So when our instruction runs it's really like `plane.flyTo("Denver")`

We'll need to work on that `flyTo` function.

#### `fly_to`

In Aviatrix, find the `flyTo` function. It looks like this:

```
func flyTo(destination : String) {
        
}
```

The `destination` that comes in is the marker like `"Denver"`. 
*Can you write one line here that stores that marker into the plane's `location` instance variable?

Test it by running `main.swift` and -- you're still in St. Louis???

#### Dream Destinations

Can you add a destination to the application? You'll need to carefully change `AviatrixData`:

* Make up a gas price and add it to the `fuelPrices` method
* The hard part is `knownDistances`. Your best bet is to carefully copy and paste one of the existing dictionaries. You'll need to add your destination to each of the existing lists. Take extra care to add commas where needed!

If you'd like to use realistic distances, you can [use this online air mileage calculator](http://www.webflyer.com/travel/mileage_calculator/).

If you got one new destination to work correctly, feel free to add a couple more!

## What We've Got

After this work, when you run the simulator:

* The `planeData` is still mostly blank, but our `Location` is accurate
* Flying to a different city works and we can move city to city
* Refueling doesn't do anything yet

Make sure your code works like that before you move on to [I2: Distances](./i2_distances_and_fuel.markdown).

## Extra Challenge

Was flying around too easy for you? How about a tricky challenge?

It would be neat if, when the simulator listed out the possible destinations, they were ordered by distance from the current city.

When we're in St. Louis we would currently see:

```
Where would you like to fly to?

0) St. Louis (0 miles)
1) Phoenix (1260 miles)
2) Denver (768 miles)
3) Salt Lake City (1150 miles)
```

But if this ordering were in place we'd see:

```
Where would you like to fly to?

0) St. Louis (0 miles)
1) Denver (768 miles)
2) Salt Lake City (1150 miles)
3) Phoenix (1260 miles)
```

You'll have to change code in the simulator to make this happen. Can you figure it out?
