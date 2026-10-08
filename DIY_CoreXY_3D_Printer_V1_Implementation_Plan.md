# DIY CoreXY 3D Printer — V1 Implementation Plan

The buy list is `parts-list.md`. This file is the build order for that list. If a quantity or a steps/mm number here disagrees with the parts list, follow the parts list.

## 1. Goal

Build a CoreXY machine with a stationary bed:

- Bed: **310 × 310 × 3 mm** aluminium heater, 24 V / **220 W**, plus a **310 × 310 mm** double-sided PEI sheet on a magnetic base
- Frame: **2020**, **520 mm** outside in X and Y, **480 mm** inside
- XY: **10 mm** rods, printed rod supports (SK10 blocks are optional spares), **8 × LM10LUU**
- Z: **three** T8 4-start screws cut from **two** 1000 mm bars, **8 mm lead**, **six** motors, **five** drivers
- Controller: **MKS Gen-L V1.0**
- Drivers: **5 × TMC2209**
- Firmware: **Marlin** first. Klipper is later
- Extruder: **BMG** direct drive
- Hotend: **V6** all-metal, 24 V / 40 W, E3D regular sock
- Part cooling: **4010 radial** blower, 24 V
- Power: **two** 24 V / 15 A / 360 W supplies, split bed and logic
- Later, and not part of this build: MGN12 rails, a probe, a 32-bit board, a Pi, input shaper, a high-flow hotend

V1 should stay cheap. The 520 mm frame and the 310 mm bed stay when those later parts arrive.

---

# 2. Freeze the cuts

Do not cut the 1 m 2020 or the 10 mm rods until this cut list is the one on the drawing. Eight metres of 2020 builds this box once. A short piece cannot be recut into a long one.

The 300 mm outer cube is withdrawn. Its inside opening is about 260 mm. A 310 mm plate does not fit in that opening.

XY frame, using the 20 mm three-way corners:

- Extrusion cut, X and Y: **480 mm**
- Outside, X and Y: 480 + 20 + 20 = **520 mm**
- Inside opening: **480 mm**
- 310 mm plate, side margin: (480 − 310) / 2 = **85 mm** per side

10 mm rods, from the two 1000 mm bars:

- Cut each bar **once**
- Four rods, each **480–500 mm**
- That length is the 480 mm opening, plus a few millimetres where the rod sits in the support
- Do not cut these rods for a 260 mm opening

2020 from the eight 1000 mm bars (8000 mm):

| Members | Qty | Cut | Uses |
| --- | --- | --- | --- |
| X and Y rails, top and bottom | 8 | 480 mm | 3840 mm |
| Gantry rail | 1 | 480 mm | 480 mm |
| Reserved above | 9 | | **4320 mm** |
| Left for 4 posts and braces | | | **3680 mm** |

Four posts at 500 mm use 2000 mm of that remainder (outside height 540 mm). What is left after the posts is braces and an electronics upright, not a second 520 mm box.

Mech Ninja’s 400 mm and 280 mm pieces are the bed frame for a 310 mm plate. This cut list does not include them yet. Add them from the 3680 mm remainder only after the bed carrier is drawn. Do not take them out of the 480 mm rails.

A 300 mm cube would consume twelve pieces around 260 mm (about 3120 mm). Those offcuts cannot become 480 mm rails. Cut the 520 mm box, or cut nothing.

---

# 3. Machine that this plan builds

| Job | Part on the list |
| --- | --- |
| Bed heater | Novo3D 310 × 310 × 3 mm, 24 V, 220 W, 100 cm cable, NTC 100K |
| Build surface | Two Trees 310 × 310 mm PEI, textured both sides, magnetic base |
| Frame | 8 × 1000 mm 2020, 8 three-way corners, 4 interior L, 10 external L |
| XY rods | 2 × 10 mm × 1000 mm, cut into four |
| XY bearings | 8 × LM10LUU |
| Z screws | 2 × T8 4-start × 1000 mm, cut into three |
| Z guides | 8 mm rods and LM8UU. Printed SK8 supports are on hand |
| Motors | 6 × NEMA17, 4.8 kg-cm, 2 A, 47 mm |
| Couplings | 3 × rigid 5 × 8 mm |
| Belts | 2 × 5 m GT2, 6 mm, steel core |
| Motor pulleys | 2 × GT2 20T, 5 mm bore, set screws |
| Bend idlers | 10 × toothless, 6 mm belt, 5 mm bore |
| Drivers | 5 × TMC2209 |
| Controller | MKS Gen-L V1.0 |
| Display | 12864 with full-size SD slot |
| Endstops | 5 × roller microswitch |
| Hotend | V6, 24 V 40 W, plus E3D regular sock |
| Extruder | BMG |
| Part fan | 4010 radial, 24 V |
| Logic fans | 2 × 4010 axial, 24 V |
| Supplies | 2 × 24 V 15 A |

Printed rod supports are already on hand. Metal SK10 and SK8 blocks are optional spares if a print cracks.

These are bought as extras or still local, and the machine is incomplete without the ones marked as needed:

- Needed before mains power: a **5 A slow-blow 5×20 mm** fuse (the IEC pack does not include it), live and neutral from the inlet to both supplies, and the earth wire
- Needed before the belts turn: **M5 nylocs** for the idler bolts. The washer pack is plain hex nuts
- Needed before the bed is trusted: a carrier drawn for the heater’s **4 mm countersunk** holes. The M4 × 40 screws fit those holes. The M3 spring kit does not
- Needed before extrusion: a toolhead that holds the BMG, the V6, and the 4010 radial fan, plus a short PTFE liner from the BMG into the V6
- The Cults files are a map. Do not print their M8 nut blocks, their MK8 toolhead, or a bed carrier drawn for a different hole pattern

---

# 4. Frame

Build the 2020 box in section 2. There is no PVC prototype.

Corners:

- **8** three-way cubes, one at each corner of the box. Checkout type 2020
- **4** interior L connectors
- **10** external L plates

These three parts are different. A three-way cube is not an L plate.

Square the lower rectangle, then the upper rectangle, then the posts. Check diagonals before the grub screws are tight. Electronics stay outside the heated volume.

---

# 5. CoreXY belts

Both drive motors stay fixed to the frame.

```text
Motor A ───── belt path ─────┐
                             │
                         XY carriage
                             │
Motor B ───── belt path ─────┘
```

Pulleys:

- The two **toothed 20T** pulleys with set screws go on the motor shafts. They are the only toothed pulleys that set steps/mm
- The ten **toothless** idlers take the smooth back of the 6 mm belt. Confirm each bore has a bearing and the wheel has side flanges
- The twelve **toothed** idlers are spares, or a bend that actually wraps the tooth side. Do not run the smooth back of the belt on them

Do not cut the belts until the frame, the motor positions, the idler positions, and the carriage are in place and the path has been checked with a scrap.

XY steps, 20 tooth, 2 mm pitch, 1.8° motor, 16× microstepping:

```text
200 × 16 / (2 × 20) = 80 steps/mm
```

Calibrate after the first moves. A value of 100 steps/mm belongs to a 16 tooth pulley and will scale every X and Y move.

---

# 6. XY rods

Four 10 mm rods, one pair per axis. Two LM10LUU on each rod.

The rods in a pair are parallel, the two pairs are square to the frame, and the carriage travels the opening without a tight spot. The 8 mm rods are the Z guides. They do not go on the XY carriage.

---

# 7. Z

Cut the two 1000 mm T8 bars into **three** screws. 2000 mm covers three screws while each is under about 650 mm. A full-length 1000 mm screw will bend. The third copper nut comes from the extra-nut pack. Each purchased bar already includes one nut.

Lead is **8 mm** (2 mm pitch, 4 starts). Z steps:

```text
200 × 16 / 8 = 400 steps/mm
```

A value of 2560 steps/mm belongs to an M8 × 1.25 rod. On this screw it would command about 6.4 times too much travel.

One missed full step is 8 / 200 = **0.04 mm**. The 4-start screw does not hold the bed when the motors turn off. Leave Z enabled.

Driver map on the five Gen-L sockets:

| Function | Driver |
| --- | --- |
| X | TMC2209 #1 |
| Y | TMC2209 #2 |
| Z and Z2, in parallel | TMC2209 #3 |
| Z3 | TMC2209 #4 |
| Extruder | TMC2209 #5 |

There is no sixth socket. The paralleled pair uses the same coil order. Those motors are 2 A each, and one TMC2209 cannot feed both at 2 A, so that pair has less torque than the single Z motor. Set the shared driver’s current inside the chip’s limit.

The screws are not the guides. Guide the bed on 8 mm rods and LM8UU. The couplings on the list are rigid 5 × 8 mm. A rigid coupling binds if the motor shaft and the screw are not collinear. Align them before the grub screws are tight.

Five switches cover X, Y, and two Z homes. The Gen-L cannot independently home a third Z. Tram the third screw to the other two with a jig, or accept that one screw is slaved.

Anti-backlash, if the extra nuts are fitted: one spare copper nut per screw, sprung against the drive nut. The spring is not on the buy list yet. Do not mix these nuts with an M8 × 1.25 nut.

---

# 8. Toolhead

```text
Filament
   ↓
BMG
   ↓
short PTFE
   ↓
V6, 24 V 40 W, 0.4 mm
   ↓
E3D regular sock
```

The mount is a drawing, not a purchased part. It has to hold the BMG, the V6, the 4010 radial blower, and both belt ends. The Mech Ninja MK8 STL does not fit this stack.

Reserve room for a probe later. The probe is not on this build.

---

# 9. Cooling

- The fan in the V6 kit cools the heatsink. One axial 4010 is the spare if that fan dies
- The **4010 radial** blower is part cooling. It is 24 V. Do not buy the 12 V size of the same listing
- The second axial 4010 cools the Gen-L and the driver heatsinks
- A 5015 is not on this list. The duct is drawn around the 40 mm blower

---

# 10. Bed

Stack, top to bottom:

```text
310 × 310 mm PEI spring sheet
magnetic base, stuck to the aluminium
310 × 310 × 3 mm heater, 24 V, 220 W
bed carrier
M4 × 40 corner screws
```

The heater holes are 4 mm and countersunk. The cable version includes an NTC 100K and JST housings. The wires arrive unsoldered. The M3 leveling kit is loose in a 4 mm hole, so the corner screws are the M4 × 40 set unless a hole is measured and is actually M3.

The plate sits in the 480 mm opening with 85 mm on each side. Make the carrier removable. Insulate under the heater only if the stack still has room for the nozzle.

Usable area is the 310 mm sheet, inside the clips and the nozzle’s reach. Z height is whatever is left after the posts, the carrier, and the toolhead are drawn. Do not enter a build volume in Marlin until that height is measured.

---

# 11. Power

Two supplies, both switched to **220 V**.

```text
IEC inlet → 5 A slow-blow fuse → switch
        │
        ├── Supply A (bed)  → heater      about 9.2 A
        │
        └── Supply B (logic) → Gen-L, V6, motors, fans

DC negatives of A and B tied together
DC positives of A and B left separate
```

Do not parallel the two 24 V positives. The tied negatives give a MOSFET control signal a reference if the MOS25 is fitted. Without the MOS25, the bed heater still needs a switch the firmware can turn off. Do not power the bed until that path exists.

Earth: IEC earth pin to both supply earth screws to one point on the 2020 frame. Green/yellow, 1.5 mm², ring terminals.

Bed wire is 16 AWG silicone, supply to bed. Logic supply to the Gen-L is 16 AWG. The V6 heater and the 24 V fans are 20 AWG. Thermistor wire is a 24 AWG twisted pair, routed away from the heater pair. Ferrule every screw terminal.

The bed supply sees about 9.2 A of its 15 A rating. A single 20–25 A supply is a later replacement for both boxes, not a third supply in parallel.

---

# 12. Mains

```text
AC mains
   ↓
IEC inlet
   ↓
5 A slow-blow 5×20 mm fuse
   ↓
switch
   ↓
both supply inputs
```

A 15 A fuse would not protect the mains lead. Cover every 230 V terminal. Strain-relieve the leads.

---

# 13. Electronics bay

Keep the supplies, the Gen-L, the drivers, and the fuse outside the heated volume. One axial 4010 blows across the driver heatsinks. The 12864 can sit on the frame. Its SD slot is full size. A microSD needs the plastic adapter. Format the card FAT32.

---

# 14. TMC2209

Start in standalone STEP/DIR. Leave UART until the axes move.

The motors are 2 A. The driver default is about 1.25 A. Raise current only until the axis stops skipping, then stop. The shared Z driver stays inside the chip limit, below 2 A for the pair. Heatsinks stay on. Judge the setting by motor temperature, missed steps, and noise.

---

# 15. Endstops

Five roller switches. Wire them **normally closed** (COM and NC) so a broken wire reads as open.

Use:

- X minimum
- Y minimum
- Z minimum
- a second Z
- one spare

Make the brackets adjustable. A probe can come later. It does not replace the X and Y switches.

---

# 16. Marlin

Configure:

- CoreXY
- **80** steps/mm on X and Y
- **400** steps/mm on Z
- three Z motors with two of them on one driver
- five TMC2209 in STEP/DIR
- bed thermistor from the NTC 100K table that matches the included sensor. Confirm the table at room temperature before heating
- hotend thermistor from the V6 sensor, or a 100K 3950 bead if that sensor is missing
- thermal runaway on
- mechanical endstops, normally closed
- 12864
- build volume only after the carriage travel and the Z height are measured. Do not enter 200 × 200 × 200 as a guess, and do not enter 310 mm of Z

Extruder steps come from a measured extrusion, not from a formula.

---

# 17. Bring-up

One stage at a time. Heaters are last.

1. **Controller.** Logic supply, Gen-L, 12864. Confirm the board boots and the display answers.
2. **X, then Y.** Direction, distance, current, motor temperature. Confirm an X command moves X and a Y command moves Y. A crossed CoreXY cable swaps them.
3. **Z.** Each motor the same direction. The paralleled pair starts together. No binding in the rigid couplings. No skipped steps over the travel.
4. **Extruder.** BMG turns the right way. Calibrate steps with a mark on the filament.
5. **Endstops.** Trigger each switch and read it. A switch that never opens will crash the axis.
6. **Thermistors.** At room temperature the bed and the hotend both read a plausible room value. A reading near 0 or near the top of the scale is a wrong table or an open wire.
7. **Heaters.** Hotend first, then the bed. Stay with the machine.

---

# 18. Heat

Hotend: temperature rises smoothly, the heater cuts at the target, the heatsink fan is running, thermal runaway is on.

Bed: the bed supply is the one feeding the heater, the terminals stay cool, the plate warms across its area. The first heat is attended.

---

# 19. Calibration

Measure 10 mm, 50 mm, and 100 mm on X, on Y, and on Z. Correct steps/mm from the measurement.

On Z, measure both sides of the bed. A difference that grows with height is a tram error between screws, not a steps error.

Travel X and Y to both ends. Look for belt rub, slack, a rod that binds, and a carriage that skews.

---

# 20. Bed leveling

1. Heat the bed.
2. Heat the nozzle.
3. Home Z.
4. Set the nozzle gap at the corners with the M4 screws.
5. Check the center.
6. Repeat after the plate is at temperature.

A probe and a mesh are later. They are not required for the first layer.

---

# 21. First prints

1. A flat 20 × 20 × 5 mm square. Extrusion, adhesion, Z gap.
2. A 20 mm cube. Size, square corners, ringing.
3. A temperature tower in PLA. PETG and TPU after the PLA cube is square.
4. A Benchy after the cube.

The spool on the list is PLA. Dry it if the square strings.

---

# 22. Speed

The frame is 2020, so the first limit is the rods, the belts, and the shared Z driver.

Start at **60–100 mm/s** and **1000–2000 mm/s²**. After the cube is clean, try **100–150 mm/s** and **2000–4000 mm/s²**. Input shaping is a Klipper feature and is not available on this Gen-L setup.

---

# 23. Enclosure

PLA and PETG can print with the frame open. ABS and ASA want panels, and the supplies stay outside those panels. Reserve a place for a chamber sensor and a vent. Do not build the panels until the motion is square.

---

# 24. Later, not this build

| Later part | Replaces |
| --- | --- |
| MGN12 rails | 10 mm rods and LM10LUU |
| Probe | the manual corner adjustment |
| 32-bit board and a Pi | Gen-L and Marlin. The TMC2209s can move if the new board is STEP/DIR |
| One 24 V 20–25 A supply | the two 15 A supplies. Do not parallel it with them |
| High-flow hotend | the V6. The BMG stays |
| A selector with its own drivers | nothing on the toolhead. The toolhead keeps one filament inlet |

---

# 25. Build order

**Phase 0 — drawing.** Freeze section 2, the bed center, the 85 mm side margins, rod positions, motor and idler positions, belt planes, the three screw positions, the toolhead envelope, and the measured Z travel.

**Phase 1 — frame.** Cut the eight 480 mm rails, the gantry, and the four posts. Assemble, square, brace.

**Phase 2 — Z.** Motors, couplings, three screws, nuts, 8 mm guides, carrier, full travel.

**Phase 3 — XY.** 10 mm rods, LM10LUU, carriage, motors, toothless idlers, the two drive pulleys, belts, clamps, tension, full travel.

**Phase 4 — toolhead.** BMG, V6, heatsink fan, 4010 radial blower, cables, travel with the toolhead on.

**Phase 5 — bed.** Carrier on the 4 mm holes, heater, thermistor, magnetic base, PEI sheet, nozzle clearance.

**Phase 6 — electronics.** Both supplies, Gen-L, drivers, logic fan, 12864, motors, endstops, thermistors, heaters. Check polarity before power.

**Phase 7 — firmware.** Section 16, then flash, then section 17.

**Phase 8 — calibration.** Section 19, then the first prints in section 21.

---

# 26. Acceptance

Mechanical:

- [ ] Frame square
- [ ] XY travels without a bind
- [ ] Three screws travel together and the bed does not drop its tram
- [ ] Belts run on the toothless idlers on the smooth side
- [ ] Toolhead is rigid
- [ ] PEI is flat on the magnet

Electrical:

- [ ] Earth bonded
- [ ] 5 A fuse fitted
- [ ] Mains covered
- [ ] Bed and logic supplies separated on the positive
- [ ] Negatives tied
- [ ] Terminals ferruled and cool under heat
- [ ] Driver fan runs

Firmware:

- [ ] X and Y at 80 steps/mm, checked with a ruler
- [ ] Z at 400 steps/mm, checked with a ruler
- [ ] Extruder calibrated
- [ ] Each endstop reads
- [ ] Both thermistors read room temperature before heat
- [ ] Thermal runaway on

Printing:

- [ ] PLA square sticks and measures
- [ ] Motors and drivers stay at a temperature you can hold a finger on

---

# 27. Numbers that must not be used

| Old figure | Why it is wrong here |
| --- | --- |
| M8 × 1.25, 2560 steps/mm | These screws are T8×8, **400** steps/mm |
| 16 tooth pulley, 100 steps/mm | The motor pulleys are 20 tooth, **80** steps/mm |
| One 360 W supply for everything | Two supplies, positives separate |
| 5015 blower | The part fan is a 24 V 4010 radial |
| 214 mm or 235 mm bed | The heater and the PEI are **310 mm** |
| Five motors and two Z screws | **Six** motors, **three** screws, **five** drivers |
| PVC frame or a 300 mm cube | 2020, 520 mm outside |
