# FieldDens Pro
### Portable Aviation Fuel Density Meter

**Status:** Hardware ordered — firmware in development  
**Author:** Eyad Ammar | Mechanical Engineering, George Mason University  
**Context:** Personal engineering project developed from real operational experience at Menzies Aviation, Dulles International Airport (IAD)

---

## The Problem

At fuel facilities like Menzies Aviation, Jet-A fuel density is measured and reported to airlines twice daily. Those readings are taken with fixed equipment that costs $5,000+ and cannot leave the tank farm.

Fueling operators on the ramp have no way to verify current density at each truck. Fuel temperature changes throughout the day — a reading taken at 60°F in the morning is meaningless at 85°F in the afternoon without thermal correction. That error translates directly into inaccurate fuel mass calculations for pilots.

## The Solution

FieldDens Pro is a handheld, battery-powered device that measures Jet-A fuel density at the truck level and automatically applies API 2540 temperature correction, outputting corrected density in lb/gal at 60°F reference temperature.

**~$130 in components. No fixed infrastructure required.**

---

## How It Works

1. Operator fills a 30ml stainless steel cup with a fuel sample
2. Cup is placed on the load cell platform on the device
3. DS18B20 probe reads fuel temperature in °F
4. Arduino calculates density and applies API 2540 correction
5. OLED displays corrected density in lb/gal
6. Reading is logged to SD card with timestamp

---

## Hardware

| Component | Function |
|-----------|----------|
| Arduino Nano ATmega328P | Microcontroller |
| DS18B20 Waterproof Probe | Temperature measurement ±0.5°C |
| 500g Load Cell + HX711 | Fuel mass measurement |
| 0.96" OLED SSD1306 I2C | Display |
| Micro SD Card Module | Data logging |
| 3×AA Battery Pack | Portable power ~60hr |
| Stainless Steel Cup 30ml | Fixed-volume fuel sample |

---

## Standards Compliance

- **API 2540 / ASTM D1250** — thermal correction formula for Jet-A fuel
- **Reference temperature:** 60°F (15°C) per US petroleum measurement standard
- **Thermal expansion constant:** K = 0.00594 per °C (Jet-A, API Table 6B)

---

## Current Status

- [x] Problem identified and documented
- [x] Hardware architecture designed
- [x] Enclosure modeled in Fusion 360
- [x] Engineering reference drawing completed
- [x] Components ordered
- [ ] Arduino firmware
- [ ] Load cell calibration
- [ ] Integration testing
- [ ] Python report generator
- [ ] GitHub full documentation upload
