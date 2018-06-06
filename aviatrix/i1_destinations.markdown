# Aviatrix I1: Destinations

As you can see in the simulator, our plane should be able to fly places. But all it can do is stay on the runway in St. Louis. Let's build up the functionality to move between cities.

## What We're Going For

When this iteration is done we should be able to fly between known cities. When we run the simulator and hit `b` to fly we will see some output like this:

```
<TODO: Fill in finished output>
```

## The Data

Open the `AviatrixData` file and check out the data that's in there. You should find:

* `location_names` that declares the locations we're going to support. The keys of this dictionary are the markers that we'll use internally and the values are the strings that we'll print to the user.
* `fuel_prices` in a later iteration we'll work on purchasing fuel. At that time we'll need this collection of fuel prices.
* `known_distances` is a huge method that defines the distances between the supported cities. Note that it's a dictionary where each city marker points to another dictionary. The second-level dictionary has the cities you could fly to along with the distance to get there.

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

We can see in the `fly` method that it's calling `plane.known_destinations` and iterating over that array. We need to modify the `known_destinations` method.

### `known_destinations`

Remember that all the data about destinations is in `AviatrixData`. We want to have this method return an array like this:

```
[:st_louis, :phoenix, :denver, :slc]
```

You can see that there's a method named `location_names` that has those markers as the keys to the dictionary.

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
1) Phoenix (0 miles)
2) Denver (0 miles)
3) Salt Lake City (0 miles)
```

We've got the city names and next want to add in the distances.

### Distance to Destination

In the simulator we can find the line that outputs that distance. It relies on the variable `distance` that was created here:

```
distance = plane.distance_to(marker)
```

So to get the distance to display correctly we've got to look at the `distance_to` method in our code.

#### `distance_to`

If you look in `AviatrixData` you'll see that the distances are in there, but how do we get to them?

First, we need to know where we are. The stub starts our plane in St. Louis. So for a first round, let's assume that any distance being calculated is *from* St. Louis.

The distance from St. Louis to Phoenix is 1260 miles. You can see that number inside the `known_distances` method of `AviatrixData`. We could get to it like this:

```
known_distances[:st_louis][:phoenix]
```

The `known_distances` method is returning a dictionary. `:st_louis` is a key in that dictionary. It points to a value which is *another* dictionary.

`:phoenix` is a key in that second dictionary. It points to a value 1260, which is what we're looking for.

So the code `known_distances[:st_louis][:phoenix]` gets us the distance between St. Louis and Phoenix. We we look at our `distance_to` method we have an argument named `target` that is the city we're heading to.

*Write code in your `distance_to` method that finds the distance between St. Louis and your `target`*

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
