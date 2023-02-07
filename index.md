---
title: "Pendix bike lights"
---

# Pendix bike lights

*Work in progress*

This site contains instructions on how to connect bike lights to a [Pendix](https://pendix.com) e-bike drive.

## General

The [Pendix](https://pendix.com) e-bike retrofit kit is a good way to add e-bike capabilities to traditional bikes. It offers simple installation and supports multiple different frames due to its unique side-mounted motor. This makes it suitable for various cargo bikes as well. One issue with the kit is that it doesn't support any way of connecting bike lights to the battery. On this site I will describe how I was able to connect front and back lights to the battery.

The Pendix battery provides a 48V DC current to the drive. This is delivered over a magnetic [Rosenberger RoPD](https://www.rosenberger.com/product/ropd/) connector in the battery and battery holder. My solution was to tap into this 48V current from within the battery holder housing. Luckily, the casing is easily opened with a couple of Torx screws. The battery holder housing has enough room to add an additional connection to the underside of the RoPD connector using 2 female spade crimp connectors, as well as a fuse for the bike light circuit.

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
- [Busch + Muller)(https://www.bumm.de/en/products/e-bike-scheinwerfer.html) also has some more 48V front lights. Though these are a bit more expensive.

Alternatively you could also add a voltage convertor to use 12V or 24V lights.
