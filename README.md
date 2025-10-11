# Actuator Controller – I²C Smart H-Bridge Board

This board is a smart linear actuator controller that uses a VNH7100BAS H-bridge with current sensing and I²C control. It is designed for 12 V actuators, supports stall/jam detection, and is chainable over I²C so you can run multiple actuators from one controller without burning GPIO pins.

This board is part of my distributed control system and is compatible with my nodeLync I²C wiring standard.

## Features
- Drives 12 V linear actuators (extend/retract)
- Solid-state H-bridge (no relays to weld shut)
- Current sensing for stall/jam detection
- I²C control using MCP23008 GPIO expander
- Optional MCP3427 ADC for current telemetry
- Motor power terminal or Anderson Powerpole input
- Status LEDs for power and activity
- Designed for Raspberry Pi or microcontroller systems
- Open hardware – modify it, build it, use it

	
## I²C Addresses
	| Device        | Base Address | Configurable         |
	|---------------|--------------|----------------------|
	| MCP23008 GPIO | 0x20–0x27    | Yes (A0–A2 jumpers)  |
	| MCP3427 ADC   | 0x68–0x6B    | Yes (ADDR pin)       |

## Current Measurement
The VNH7100BAS provides a current sense output. In 12-bit mode:
Useful for overload protection and detecting mechanical faults.

## Documentation
Full design writeup:
https://vinthewrench.substack.com

Demo video:
https://youtu.be/HOyxq8rQfaQ

## Status
✅ Prototype tested  
✅ Verified on Raspberry Pi  
✅ Load tested with Progressive Automations PA-10 and PA-14 actuators  
✅ Ready for fabrication / community mods

## License
This is Open Hardware under the CERN-OHL-P v2 license.

You can build it, modify it, use it commercially, and keep modifications private if you want. Just do not remove the original credit.

SPDX-License-Identifier: CERN-OHL-P-2.0  
© 2025 Vinnie Moscaritolo

## Contributions
Issues and pull requests are welcome. If you build one, I would like to see it.

