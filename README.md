# 🔧 SRAM AXS Charger Teardown & USB-C Conversion

<div align="center">
  <img src="https://img.shields.io/badge/Difficulty-Advanced-red" alt="Difficulty: Advanced">
  <img src="https://img.shields.io/badge/Tools-Soldering_Required-orange" alt="Soldering Required">
  <img src="https://img.shields.io/badge/Time-2--3_Hours-blue" alt="Time: 2-3 Hours">
</div>

> **⚠️ Disclaimer:** This modification will void your warranty and requires advanced soldering skills. Proceed at your own risk.

A detailed teardown and modification guide for converting the SRAM AXS charger from micro USB to a modern USB-C connector.

## Overview

The SRAM AXS wireless shifting system uses an outdated micro USB charging connector that can be inconvenient for travel and daily use. This project documents the process of teardown and conversion to a modern USB-C connector for improved compatibility and convenience.

## Project Goals

- [ ] Complete teardown documentation
- [ ] Identify internal components and charging circuit
- [ ] Design USB-C conversion solution
- [ ] Test charging functionality
- [ ] Document reassembly process

## 🛠️ Tools Required

### 🔓 Basic Teardown
| Tool |
|------|
| Torx T10??? screwdriver |
| Tiny flathead screwdriver |

### ⚡ USB-C Conversion
| Tool |
|------|
| Soldering station |
| Hot plate **OR** hot air station |
| Soldering wire |
| Flux |
| Desoldering wick |
| Isopropyl alcohol |
| Q-tips |
| USB-C breakout board |
| Multimeter |

## Teardown Process

### Step 1: Locate and Access the Hidden Screw
1. Find the screw location under the sticker on the charger housing
2. Carefully cut a small hole in the sticker to access the screw
3. Unscrew the Torx screw using the Torx T10??? screwdriver

*[Add images showing sticker location, cutting process, and screw removal]*

### Step 2: Opening the Charger
**Method:** Use a tiny flathead screwdriver to carefully pry open the charger at the side seam.

1. Locate the seam where the two halves of the charger housing meet
2. Insert the tiny flathead screwdriver into the seam at the side of the charger
3. Gently apply pressure to separate the housing halves
4. Work around the perimeter if needed to fully open the housing

**Caution:** Apply gentle, steady pressure to avoid cracking the plastic housing.

*[Add images showing the opening process and tool placement]*

### Step 3: PCB Inspection
Once the housing is opened, you'll have access to the internal PCB (Printed Circuit Board).

*[Add photos of the PCB showing component layout and connections]*

### Step 4: Foam Removal
Before analyzing the PCB, remove the black foam padding from the back of the PCB.

1. Use the tiny flathead screwdriver to carefully pry off the black foam
2. Work gently to avoid damaging the PCB or components underneath
3. The foam may be adhesive-backed, so remove it slowly
4. Clean the PCB surface with isopropyl alcohol and cotton swabs to remove any adhesive residue

*[Add photos showing foam removal and cleaning process]*

### Step 5: Internal Analysis
*[Identify charging circuit, power management, and connection points]*

---

## ⚡ USB-C Conversion

### Circuit Analysis
*[Document voltage requirements, pinout, and power delivery specs]*

### Preparation
Before starting the conversion, ensure your workspace is properly set up:

1. Set up soldering station at appropriate temperature
2. Prepare hot plate / hot air soldering station
3. Have flux, soldering wire, and cleaning supplies ready
4. Ensure proper ventilation for soldering work

### Modification Process

#### Step 1: Micro USB Connector Removal
Removing the existing micro USB connector can be challenging due to the robust solder joints.

**Hot Plate Method:**
1. Place only the small area of the PCB (where the micro USB connector is located) on the hot plate
2. Ensure the backside of this area has no components that could be damaged by heat
3. Heat the area until the solder becomes molten
4. Remove the micro USB connector with tweezers

**Alternative: Hot Air Station Method:**
1. Use a hot air soldering station to heat the micro USB connector area
2. Apply heat evenly to the connector until solder becomes molten
3. Remove the connector with tweezers once solder is molten

#### Step 2: Clean the Pads
1. Clean the remaining solder from the pads using soldering iron and desoldering wick/braid
2. Clean the PCB thoroughly with isopropyl alcohol and cotton swabs to remove flux residue and debris

**Important:** Only heat the specific area around the connector to avoid damaging other components on the PCB.

*[Add photos showing hot plate positioning, connector removal, and cleaning process]*

#### Step 3: USB-C Installation Preparation
1. Apply flux to the cleaned PCB pads where the micro USB connector was removed
2. Apply flux to the corresponding pins/pads on the USB-C breakout board
3. Pre-tin both the PCB pads and the USB-C board pins with a small amount of solder

#### Step 4: Soldering Method
**Hot Plate Method:**
1. Clean everything thoroughly with isopropyl alcohol and cotton swabs
2. Place the PCB on the hot plate (focusing on the connector area)
3. Wait for the solder to become molten
4. While the solder is molten, carefully position and place the USB-C breakout board
5. Allow to cool and form solid connections

**Alternative: Hot Air Station Method:**
1. Clean everything thoroughly with isopropyl alcohol and cotton swabs
2. Position the USB-C breakout board on the PCB
3. Use hot air station to heat the connection area until solder becomes molten
4. Allow to cool and form solid connections

**Final Steps (for both methods):**
6. Once cooled, use the soldering iron to properly solder each individual pin
7. Check for any solder bridges between adjacent pins
8. Use a multimeter to verify there are no short circuits between pins

**Tip:** Both methods ensure even heating and better solder flow for reliable connections. Follow up with soldering iron work for secure individual pin connections.

*[Add photos showing cleaning, hot plate positioning, and USB-C placement process]*

#### Step 5: Cleaning and Finishing
- Clean flux residue with isopropyl alcohol and cotton swabs
- Secure connections with hot glue

#### Step 6: Housing Modification
- File the plastic housing opening to accommodate the new USB-C connector
- Test fit the USB-C connector through the modified opening
- Ensure smooth insertion and removal of USB-C cables

*[Add photos of filing process and connector fitting]*

### Testing
1. Check for short circuits between the pins (especially + and -) using a multimeter
2. Plug in the PCB to a USB-C power source and check if the blue LED is lighting up
3. Test USB-C cable in both directions to ensure proper connection
4. Reassemble the charger housing
5. Test charging functionality with a compatible battery

*[Add photos of multimeter testing, LED status, cable testing, and reassembly]*

## 🎯 Results

### Success!
After completing this modification, you no longer need to bring a separate micro USB cable on your bikepacking trips. The charger now uses the same USB-C cable as your other modern devices, reducing cable clutter and improving convenience.

**Benefits:**
- ✅ Universal USB-C compatibility
- ✅ Reduced cable count for travel
- ✅ Modern connector standard
- ✅ Reversible plug orientation

*[Add photos of final result and comparison with original]*

## ⚠️ Safety Warnings

<div style="background-color: #ffe6e6; border: 2px solid #ff4444; border-radius: 8px; padding: 15px; margin: 15px 0;">

### 🚨 Critical Safety Information

- **Fire Hazard:** Modifying charging equipment can create fire or safety risks
- **Electrical Safety:** Ensure proper voltage and current ratings before testing
- **Component Protection:** Test thoroughly with cheap devices before using with expensive components
- **Warranty Void:** This modification will void all manufacturer warranties
- **Skill Level:** Advanced soldering skills required - not suitable for beginners

</div>

## 📄 License

This documentation is provided for **educational purposes only**.

**Modify at your own risk** - the authors are not responsible for any damage to equipment or personal injury.

---

<div align="center">
  <sub>⭐ If this guide helped you, consider giving it a star!</sub>
</div>
