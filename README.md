# 🔧 SRAM AXS Charger Teardown & USB-C Conversion

<div align="center">
  <img src="https://img.shields.io/badge/Difficulty-Advanced-red" alt="Difficulty: Advanced">
  <img src="https://img.shields.io/badge/Tools-Soldering_Required-orange" alt="Soldering Required">
  <img src="https://img.shields.io/badge/Time-1--2_Hours-blue" alt="Time: 1-2 Hours">
</div>

A detailed teardown and modification guide for converting the SRAM AXS charger from micro USB to a modern USB-C connector.

![Original charger](images/original_web.png)

## ⚠️ Safety Warnings

> This teardown and modification will void your warranty and requires advanced soldering skills. Proceed at your own risk.

<div style="background-color: #ffe6e6; border: 2px solid #ff4444; border-radius: 8px; padding: 15px; margin: 15px 0;">

### 🚨 Critical Safety Information

- **Fire Hazard:** Modifying charging equipment can create fire or safety risks
- **Electrical Safety:** Ensure proper voltage and current ratings before testing
- **Component Protection:** Test thoroughly with cheap devices before using with expensive components
- **Warranty Void:** This modification will void all manufacturer warranties
- **Skill Level:** Advanced soldering skills required - not suitable for beginners

</div>

## Overview

The SRAM AXS wireless shifting system uses an outdated micro USB charging connector that can be inconvenient for travel and daily use. This project documents the process of teardown and conversion to a modern USB-C connector for improved compatibility and convenience.

## Project Goals

- [x] Complete teardown documentation
- [x] Find USB-C conversion solution
- [x] Test charging functionality

## 🔓 Teardown

| Required Tools |
|------|
| Torx T-10 screwdriver |
| Tiny flathead screwdriver |

### Step 1: Locate and Access the Hidden Screw
1. Find the screw location under the sticker on the charger housing
2. Carefully cut a small hole in the sticker to access the screw
3. Unscrew the Torx screw using the Torx T-10 screwdriver

![Housing unscrewed](images/housing%20unscrewed_web.png)

### Step 2: Opening the Charger
Use a tiny flathead screwdriver to carefully pry open the charger at the side seam.

1. Locate the seam where the two halves of the charger housing meet
2. Insert the tiny flathead screwdriver into the seam at the side of the charger
3. Gently apply pressure to separate the housing halves
4. Work around the perimeter if needed to fully open the housing

**Caution:** Apply gentle, steady pressure to avoid cracking the plastic housing.

![Opening charger](images/opening%20charger_web.png)

### Step 3: PCB Inspection
Once the housing is opened, you'll have access to the internal PCB.

**PCB Top Side:**
![PCB Upper](images/pcb%20upper_web.png)

**PCB Bottom Side:**
![PCB Bottom](images/pcb%20bottom_web.png)

#### Micro USB-B Port Pinout Analysis

After examining the PCB, the micro USB-B connector pinout is as follows:

![Micro USB Spec](images/micro%20usb%20detail_web.png)

| Pin | Function | Connection |
|-----|----------|------------|
| 1   | GND      | Connected to Ground |
| 2   | ID       | Connected to Ground |
| 3   | D+       | Unused |
| 4   | D-       | Unused |
| 5   | VBUS     | Connected to +5V |

So it's important to use a MC002 USB-C breakout board with 5V on the right side and GND on the left side.

---
⚠️ Stop here if you don't have advanced soldering skills and know what you are doing!

## ⚡ USB-C Conversion

| Required Tools |
|------|
| Soldering station |
| Hot plate **OR** hot air station |
| Soldering wire / paste |
| Flux |
| Desoldering wick |
| Isopropyl alcohol &  Q-tips |
| Multimeter |

| Required Parts |
|------|
| USB-C breakout board (MC002) |

### Preparation
Before starting the conversion, ensure your workspace is properly set up:

1. Set up soldering station at appropriate temperature
2. Prepare hot plate / hot air soldering station
3. Have flux, soldering wire, and cleaning supplies ready
4. Ensure proper ventilation for soldering work

### Modification Process

### Step 1: Foam Removal
Before analyzing the PCB, remove the black foam padding from the back of the PCB.

1. Use the tiny flathead screwdriver to carefully pry off the black foam
2. Work gently to avoid damaging the PCB or components underneath
3. The foam is adhesive-backed, so remove it slowly
4. Clean the PCB surface with isopropyl alcohol and cotton swabs to remove any adhesive residue

![Remove foam step 1](images/remove%20foam%201_web.png)

![Remove foam step 2](images/remove%20foam%202_web.png)

![Remove foam step 3](images/remove%20foam%203_web.png)

#### Step 2: Micro USB Connector Removal
Removing the existing micro USB connector can be challenging due to the robust solder joints.

**Important:** Only heat the specific area around the connector to avoid damaging other components on the PCB.

**Hot Plate Method:**
1. Place only the small area of the PCB (where the micro USB connector is located) on the hot plate
2. Ensure the backside of this area has no components that could be damaged by heat
3. Heat the area until the solder becomes molten
4. Remove the micro USB connector with tweezers

**Alternative: Hot Air Station Method:**
1. Use a hot air soldering station to heat the micro USB connector area
2. Apply heat evenly to the connector until solder becomes molten
3. Remove the connector with tweezers once solder is molten

![Micro USB removal step 1](images/micro%20usb%20removal%201_web.png)

![Micro USB removal step 2](images/micro%20usb%20removal%202_web.png)

#### Step 3: Clean the Pads
1. Clean the remaining solder from the pads using soldering iron and desoldering wick
2. Clean the PCB thoroughly with isopropyl alcohol and cotton swabs to remove flux residue and debris

#### Step 4: USB-C Installation Preparation
1. Apply flux to the cleaned PCB pads where the micro USB connector was removed
2. Apply flux to the corresponding pins/pads on the USB-C breakout board
3. Pre-tin both the PCB pads and the USB-C board pins with a small amount of solder

![Solder USB-C step 1](images/solder%20usb%20c%201_web.png)

![Solder USB-C step 2](images/solder%20usb%20c%202_web.png)

#### Step 5: Soldering Method
**Hot Plate Method:**
1. Clean everything thoroughly with isopropyl alcohol and cotton swabs
2. Apply flux to both the PCB pads and USB-C breakout board pads
3. Place the PCB on the hot plate (focusing on the connector area)
4. Wait for the solder to become molten
5. While the solder is molten, carefully position and place the USB-C breakout board
6. Allow to cool and form solid connections

**Alternative: Hot Air Station Method:**
1. Clean everything thoroughly with isopropyl alcohol and cotton swabs
2. Apply flux to both the PCB pads and USB-C breakout board pads
3. Position the USB-C breakout board on the PCB
4. Use hot air station to heat the connection area until solder becomes molten
5. Allow to cool and form solid connections

**Final Steps (for both methods):**
6. Once cooled, use the soldering iron to properly solder each individual pin
7. Check for any solder bridges between adjacent pins
8. Use a multimeter to verify there are no short circuits between pins

**Tip:** Both methods ensure even heating and better solder flow for reliable connections. Follow up with soldering iron work for secure individual pin connections.

![Solder USB-C step 3](images/solder%20usb%20c%203_web.png)

![Solder USB-C step 4](images/solder%20usb%20c%204_web.png)

#### Step 6: Cleaning and Finishing
- Clean flux residue with isopropyl alcohol and cotton swabs
- Secure USB-C port with hot glue

#### Step 7: Housing Modification
- File the plastic housing opening to accommodate the new USB-C connector
- Test fit the USB-C connector through the modified opening
- Ensure smooth insertion and removal of USB-C cables

**Filed Housing:**
![Housing with sticker filed](images/housing%20filed_web.png)

**USB-C Installed in Housing:**
![USB-C in housing](images/usb%20c%20in%20housing_web.png)

### Testing
1. Check for short circuits between the pins (especially + and -) using a multimeter
2. Plug in the PCB to a USB-C power source and check if the blue LED is lighting up
3. Test USB-C cable in both directions to ensure proper connection
4. Reassemble the charger housing
5. Test charging functionality with a compatible battery

![Testing USB-C](images/testing%20usb%20c_web.png)

## 🎯 Results

### Success!
After completing this modification, you no longer need to bring a separate micro USB cable on your bikepacking trips. The charger now uses the same USB-C cable as your other modern devices, reducing cable clutter and improving convenience.

**Benefits:**
- ✅ Universal USB-C compatibility
- ✅ Reduced cable count for travel
- ✅ Modern connector standard
- ✅ Reversible plug orientation

## 📄 License

This documentation is provided for **educational purposes only**.

**Modify at your own risk** - the authors are not responsible for any damage to equipment or personal injury.

---

<div align="center">
  <sub>⭐ If this guide helped you, consider giving it a star!</sub>
</div>
