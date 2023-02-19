> :information_source: **Note:** Work in progress

> :warning: **Warning:** While this guide doesn't do any irreversible damage to the Pendix system, it will probably void the warranty. So it is good to be familiar with electronics, and know what you are doing before starting.

This site contains instructions on how to connect bike lights to a [Pendix](https://pendix.com) e-bike drive.

## General

The [Pendix](https://pendix.com) e-bike retrofit kit is a good way to add e-bike capabilities to traditional bikes. It offers simple installation and supports multiple different frames due to its unique side-mounted motor. This makes it suitable for various cargo bikes as well. One issue with the kit is that it doesn't support any way of connecting bike lights to the battery. On this site I will describe how I was able to connect front and back lights to the battery.

The Pendix battery provides a 48V DC current to the drive. This is delivered over a magnetic [Rosenberger RoPD](https://www.rosenberger.com/product/ropd/) connector in the battery and battery holder. My solution was to tap into this 48V current from within the battery holder housing. Luckily, the casing is easily opened with a couple of Torx screws. The battery holder housing has enough room to add an additional connection to the underside of the RoPD connector using 2 female spade crimp connectors, as well as a fuse for the bike light circuit.

### Initial power draw

The Pendix battery seems to have some kind of short  circuit safety feature which limits the max current allowed wen initially connected. If the power draw is too high, the battery will cut the power. Once the engine has initialized, the full 250W power is available.

This behaviour is unfortunately not documented, so the detailed functionality is not known. The initial power draw seems to be limited to between 1-10W, but further testing would be needed to determine the exact value. If you have more information, please add a mention about it in the discussions.

Additionally, the exact behaviour for initializing the motor is not known. At least turning the pedals will initialize the motor, turning the rear wheel might also do the same.

This limitation mean high power lights need to have some kind of power control. The simplest solution is to use a manual switch for the lights, and only turn them on after touching the pedals. Alternatively, one could possibily identify the motor initialization from the data pins, but that would require additinal investigation.

## Parts needed

- 2x female spade crimp connectors
- 2-wire cable
- Heat shrink tube
- Zip ties
- Bike lights
- Fuse (optional)
    - Not sure if really needed since the battery itself does have circuit protection. But made me safer that the motor won't stop working just because my bike light wiring would have some issues.
    - I used an 1A polyfuse for this, as it is small enough to fit inside the battery holder casing.
- Switch (optional)
    - If you want to be able to turn off the lights during daytime to save battery, although the poewr draw of the lights is quite low.
- Intermediary connectors
    - If you have multiple lights and switches, there will be quite a lot of wiring. So you might want to add some easily detachable connectors for the lights and switch. I used XT-60 and XT-30 connectors used in RC-cars, but 2 pin AMP Superseal connectors used in real cars are also easy to get hold off.

## Instructions

1. Build the bike light power cable
    1. Strip the wries from one end of the cable
    2. Connect the female spade crimp connectors, and cover the end with heat shrink tubing
    3. Add some glue to the side of the crimp connectors flat side to make it grip to the connector wall
    4. Add an optional fuse to the circuit
3. Open the battery holder enclosure
4. Attach the bike light power cable
    1. Jam the female spade crimp connectors between the positive and negative poles of the RoPD connector. Make sure that there isn't any short circuiting between the positive and negative poles.
    2. Secure the bike light cable to the main motor cable with some zip ties so that it stays secure connected
5. Route the cable out of the housing and close it.
6. Attach lights and switches to the other end of the wire.

## Bike lights

There aren't that many 48V bike lights available, so here are some I've found:
- [Beuchel](https://buechel-online.com/en/bicycle-lighting/) has multiple 48V bike lights both for [front](https://buechel-online.com/en/shiny-80/) and [back](https://buechel-online.com/en/z-fire-mini/) with various [light output levels](https://buechel-online.com/en/shiny-120/). Not too expensive.
- [Busch + Muller](https://www.bumm.de/en/products/e-bike-scheinwerfer.html) also has some more 48V front lights. Though these are a bit more expensive.

Alternatively you could also add a voltage convertor to use 12V or 24V lights.

## Other alternatives

The Pendix battery has a built in USB-C output for charging a phone etc. This could also be used to power bike lights, but is only rated for 5V 1.5A, which might not be enough for brighter lights. Additionally it requires a separate cable to be plugged every time the battery is mounted.
