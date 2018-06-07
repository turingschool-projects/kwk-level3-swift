# Aviatrix I2: Distance & Fuel

Right now our magical plane can fly around and around, never running out of fuel. Let's work on tracking how far we're going, how much fuel we're using, and build the ability to refuel.

## Tracking Distance Flown

When you read the gauges in the simulator you see something like this:

```
Reading the gauges...

| Running:   | ✅
| Location:  | St. Louis
| Fuel:      | 0 gallons
| Max Fuel:  | 0 gallons
| MPG:       | 0.4
| Fuel Bill: | $0.00
| Distance:  | 0 miles
```

That `Distance` line doesn't change even when we fly to other cities.

### In The Simulator

When you look in the `gauges` method of the simulator you see a line like this:

```
puts_fast "| Distance:  | #{plane.distance_traveled} miles"
```

That tells us the distance is coming from the `distance_traveled` method.

### `distance_traveled`

In Aviatrix, `distance_traveled` is an attribute -- it's just a number that's stored, not a method that does calculations. Up in the `initialize` method it gets set to `0` when the plane is first created.

But it never gets changed. What code can you add to the `fly_to` method so that it updates the value of `distance_traveled`? Make sure that the values accumulate as you go from one city to another, not resetting each time. Pay careful attention to the order of your instructions in `fly_to`.

#### Results

When it's working and you fly a plane from St. Louis to Denver, the gauges would say:

```
| Running:   | ✅
| Location:  | Denver
| Fuel:      | 0 gallons
| Max Fuel:  | 0 gallons
| MPG:       | 0.4
| Fuel Bill: | $0.00
| Distance:  | 768 miles
```

Then after flying back to St. Louis:

```
| Running:   | ✅
| Location:  | St. Louis
| Fuel:      | 0 gallons
| Max Fuel:  | 0 gallons
| MPG:       | 0.4
| Fuel Bill: | $0.00
| Distance:  | 1536 miles
```

#### Challenge

Starting in St. Louis, what's the closest you can get to flying 5000 miles without going over?

## Burning Fuel

It takes a lot of gasoline to move an airplane. Commercial flights loaded up with passengers can need five gallons of gas to go just one mile!

Let's build out the fuel-tracking in our project.

### In The Simulator

When you read the gauges in the simulator you see:

```
Reading the gauges...

| Running:   | ✅
| Location:  | St. Louis
| Fuel:      | 0 gallons
| Max Fuel:  | 0 gallons
| MPG:       | 0.4
| Fuel Bill: | $0.00
| Distance:  | 0 miles
```

### Max Fuel

*Can you modify the code in your Aviatrix so the Max Fuel shows up as 5000 gallons?*

When it works your gauges will show this:

```
Reading the gauges...

| Running:   | ✅
| Location:  | St. Louis
| Fuel:      | 5000 gallons
| Max Fuel:  | 5000 gallons
| MPG:       | 0.4
| Fuel Bill: | $0.00
| Distance:  | 0 miles
```

### Fuel to Fly

Let's track how much fuel we're using to fly:

* Your plane has a `miles_per_gallon` attribute with the value `0.4`
* You know how far it is from one city to another
* Your fuel level is stored in the `fuel_level` attribute.

*Can you modify your `fly_to` method so that it calculates how much fuel is used during the flight and decreases `fuel_level` the right amount?*

When it's working correctly and you fly from St. Louis to Denver your gauges will say:

```
Reading the gauges...

| Running:   | ✅
| Location:  | Denver
| Fuel:      | 3080.00 gallons
| Max Fuel:  | 5000 gallons
| MPG:       | 0.4
| Fuel Bill: | $0.00
| Distance:  | 768 miles
```

#### Challenge

* What happens when you run out of fuel?
* Starting in St. Louis, what's the closest you can get to an empty gas tank without hitting zero?

#### Extra Challenge

Only try this if things are going really well.

Gas is heavy, so the more gas you're carrying the more energy it takes to move your plane and the lower your miles per gallon.

Instead of your MPG always being `0.4` can you modify your code so the MPG is approximated based on the number of gallons in the tank when the flight starts? Here's a formula for you:

```
mpg = 0.55 - (Number of Gallons)x(0.00005)
```

What's the different in the miles-per-gallon of a full tank versus when the tank is empty?

## Refueling

Each airport is happy to sell us jet fuel.

### In The Simulator

You can look at the `refuel` method in the simulator and you'll see:

```
refuel_data = plane.refuel
puts_slow "⛽ Here in #{plane.location_name}, jet fuel costs $#{refuel_data[:unit_price]}/gallon"
puts_slow "⛽ You refueled #{refuel_data[:quantity]} gallons totaling $#{'%.2f' % refuel_data[:spent]}"
```

There are a lot of things happening in there!

### `refuel` - First Try

First there's a call to the `refuel` method. Find that method in your Aviatrix.

You'll see that the stub method is currently returning a dictionary with three key/value pairs. Ignore that for now.

*Above the dictionary, can you write one line of code that fills the gas tank back to it's maximum level?*

Try it in your simulator. When you fly to another city, then refuel, is your gas tank full? Check the fuel level by reading the gauges.

### `refuel` - Doing Better

You can see from the simulator code that it's expecting to get back a dictionary with three key/value pairs:

* `quantity` referencing how many gallons were added
* `unit_price` with the price per gallon in the current city
* `spent` with the total bill for this fill-up

*Can you improve your `refuel` method so that these three values are correctly calculated?*

Here are a couple tips:

* start by calculating how much gas you need
* find the price in the current city in `AviatrixData`
* the simulator will take care of rounding off the cents, so don't worry about that

### Tracking Total Fuel Costs

Eventually you'll have to pay that fuel bill. Let's keep track of our total spent
on refueling.

Your plane has a `fuel_cost` attribute that starts at zero. Each time you refuel, add the amount that you spent to the total `fuel_cost`. Read your gauges after two refuelings and make sure that the total is correct.

## What We've Got

* We can navigate between cities
* We track the fuel usage as we move city to city
* We can refuel in any city
* We track the total cost of refueling

## Challenges

* Try to visit each of the four cities we started with (St. Louis, Phoenix, Denver, and Salt Lake City). What's the *lowest possible fuel bill* to complete the trip without crashing?
* What's the most total miles you can travel with just one refueling?
