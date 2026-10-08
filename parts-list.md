# 3D Printer Parts List

**Running total:** ₹36,585 (unpriced rows are TBD)

**V1** = first Marlin / Gen-L / dual-T8 / rod machine. **Required** = on the Mech Ninja list, or a better part for the same job. **Optional** = spare, V2, or a part their list does not have.

**Mech Ninja** compares this sheet with their recommended list. `Better than theirs` is the same job with our part. `We have, they don't` is only on this sheet, and those rows are Optional. `They have, we don't` is on their list and not bought here. `Same` is on both lists.

The **#** column is a stable id. Rows inside a section follow the build: power, control, heat, motion, then the small parts that mount them.

## Electronics


| #   | V1       | Mech Ninja             | Item                                               | Specs                                                           | Qty / pack | Price             | Source                      | Link                                                                                                                                                                         |
| --- | -------- | ---------------------- | -------------------------------------------------- | --------------------------------------------------------------- | ---------- | ----------------- | --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 14  | Required | Better than theirs    | TRIDEV switching PSU                               | 24 V 15 A 360 W, AC 220/240 V in                                | 2          | ₹1,699 × 2 = ₹3,398 | Amazon (ASIN B07R2DL1ML)    | [Product](https://www.amazon.in/dp/B07R2DL1ML)                                                                                                                               |
| 16  | Required | Better than theirs    | MKS Gen-L V1.0 controller                          | Onboard Mega 2560, 12–24 V, 5 driver slots                      | 1          | ₹2,159            | RoboticsDNA (SKU RDNA-F339) | [Product](https://roboticsdna.in/product/mks-gen-l-v1-0-compatible-for-ramps1-4-mega2560-r3-support-a4988-drv8825-tmc2100-lv8729/)                                           |
| 15  | Required | Better than theirs    | MKS TMC2209 V2.0 stepper driver                    | 5.5–28 V, 1.25 A default / 2.5 A max, heatsink included         | 5          | ₹459 × 5 = ₹2,295 | Novo3D                      | [Product](https://novo3d.in/mks-tmc2209/)                                                                                                                                    |
| 2   | Required | Better than theirs    | NEMA17 stepper motor 4.8 kg-cm                     | 1.8°, 2 A/phase, 47 mm body, 4-wire, attached cable, SKU G4 006 | 6          | ₹609 × 6 = ₹3,654 | Novo3D                      | [Product](https://novo3d.in/nema17-stepper-motor/?attribute_type=Attached%20cable%20with%20motor)                                                                            |
| 17  | Required | Same                   | 128×64 smart LCD controller                        | Encoder, SD slot, adapter + cable                               | 1          | ₹799              | Robocraze (SKU TIF3P0078)   | [Product](https://robocraze.com/products/3d-printer-128x64-smart-lcd-display-controller?variant=40192882704537)                                                              |
| 18  | Required | Same                   | KW4-Z5F150 SPDT roller lever micro switch          | 5 A, 1.5 N, Daier                                               | 5          | ₹23 × 5 = ₹115    | Robu (SKU R132437)          | [Product](https://robu.in/product/kw4-z5f150-spdt-roller-lever-micro-switch-5a1-5n/)                                                                                         |
| 12  | Required | Same                  | Novo3D heat bed                                | 310 × 310 × 3 mm aluminium, 24 V, 220 W, 100 cm cable, NTC 100K, SKU D3 007 | 1          | ₹1,799            | Novo3D                      | [Product](https://novo3d.in/heat-bed-310mm/?attribute_voltage=24v&attribute_type=Heat%20bed%20with%20100cm%20cable)                                                          |
| 74  | Required | We have, they don't   | Two Trees double-sided PEI sheet               | 310 × 310 mm, textured both sides, magnetic base, SKU 1645137 | 1          | ₹1,899            | Robu                        | [Product](https://robu.in/product/two-trees-double-side-pei-coating-310x310-hotbed-for-3d-printer/)                                                                          |
| 13  | Required | Better than theirs    | Kingroon V6 direct hotend + fan                    | 24 V 40 W, 1.75 mm / 0.4 mm, all-metal                          | 1          | ₹588              | Evelta (SKU 509-B01488)     | [Product](https://evelta.com/v6-direct-hotend-with-fan-24v-40w-1-75-0-4mm/)                                                                                                  |
| 60  | Required | Better than theirs    | E3DV6 Regular silicone sock                        | Black, regular V6 block (not PT100/Volcano/MK8)                 | 1          | ₹18               | Novo3D                      | [Product](https://novo3d.in/e3dv6-silicone-sock/?attribute_type=E3DV6%20Black%20Regular)                                                                                     |
| 10  | Required | Better than theirs    | TPU Bondtech BMG deceleration double-gear extruder | 1.75 mm filament, unassembled + mounting hardware               | 1          | ₹745              | Flyrobo (SKU 2880)          | [Product](https://www.flyrobo.in/tpu-bondtech-bmg-deceleration-double-gear-extruder)                                                                                         |
| 30  | Required | Same                   | Ender 24 V layer cooling fan                       | 4010 radial blower, 24 V, 0.07 A, 1.6 CFM, JST-XH, 100 cm lead, size 4010 24V Radial Fan, ASIN B08QJMZC71 | 1          | ₹325              | Amazon                      | [Product](https://www.amazon.in/dp/B08QJMZC71)                                                                                                                               |
| 56  | Required | Same                   | 4010 axial cooling fan                             | 24 V, 0.09 A, 40×40×10 mm, 2-pin, ~22 cm cable, SKU TIF3P0180  | 2          | ₹69 × 2 = ₹138    | Robocraze (SKU TIF3P0180)   | [Product](https://robocraze.com/products/high-quality-4010-cooling-fan-24v-0-09a-with-20cm-cable?variant=43183483584736)                                                      |


**Electronics subtotal (Required):** ₹17,932

## Hardware


| #   | V1       | Mech Ninja          | Item                                        | Specs                                        | Qty / pack      | Price             | Source            | Link                                                                                                                                               |
| --- | -------- | ------------------- | ------------------------------------------- | -------------------------------------------- | --------------- | ----------------- | ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| 29  | Required | Same                | 2020 three-way corner connector             | Aluminum, 20 × 20, 3-axis, grub screws       | 8               | ₹89 × 8 = ₹712    | Novo3D            | [Product](https://novo3d.in/3-way-corner-connector/?attribute_type=2020)                                                                           |
| 59  | Required | Same                | 2020 interior L-connector                   | Zinc, 90°, T-slot, M4 grub, 1 pc             | 4               | ₹45 × 4 = ₹180    | Novo3D            | [Product](https://novo3d.in/aluminium-connector/)                                                                                                  |
| 71  | Required | Same                | 2020 L-type profile connector               | Aluminum, external L, 2020 V-slot, 1 pc      | 10              | ₹55 × 10 = ₹550   | Novo3D            | [Product](https://novo3d.in/l-type-profile-connector/)                                                                                             |
| 23  | Required | Same                | SS304 smooth rod 10 mm × 1000 mm            | Stainless steel, 10 mm OD                    | 2               | ₹480 × 2 = ₹960   | OnlyScrews        | [Product](https://onlyscrews.in/products/10mm-smooth-rod-stainless-steel-304-1meter-1000mm?variant=54470816694585)                                 |
| 6   | Required | Same                | SS smooth rod 8 mm × 1000 mm                | Stainless steel linear rod                   | 2 packs (4 pcs) | ₹585 × 2 = ₹1,170 | Meesho            | [Product](https://www.meesho.com/2-pcs-ss-smooth-rod-8mm-od-1000mm-stainless-steel-linear-rods-for-3d-printers-cnc-robotics-diy-projects/p/aj9ysd) |
| 1   | Required | Better than theirs | Trapezoidal 4-start lead screw + copper nut | 8 mm, 2 mm pitch (8 mm lead), 1000 mm, SS304 | 2               | ₹469 × 2 = ₹938   | Robu (SKU 51588)  | [Product](https://robu.in/product/1000mm-trapezoidal-lead-screw-8mm-thread-2mm-pitch-lead-screw-with-copper-nut/)                                  |
| 8   | Required | Same                | Aluminum NEMA17 shaft coupling 5×8 mm       | 5 mm motor shaft to 8 mm screw, D19 L25      | 3               | ₹72 × 3 = ₹216    | Flyrobo (SKU 752) | [Product](https://www.flyrobo.in/aluminium-nema17-shaft-coupling-5mm-x-8mm)                                                                        |
| 9   | Required | Same                | GT2 steel-core open belt                    | 6 mm width, 2 mm pitch, 500 cm (5 m)         | 2               | ₹407 × 2 = ₹814   | Novo3D            | [Product](https://novo3d.in/gt2-6mm-belt/)                                                                                                         |
**Hardware subtotal (Required):** ₹5,540

## Pulleys


| #   | V1       | Mech Ninja | Item                                     | Specs                                               | Qty / pack     | Price             | Source                    | Link                                                                                                                                               |
| --- | -------- | ---------- | ---------------------------------------- | --------------------------------------------------- | -------------- | ----------------- | ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| 5   | Required | Same       | GT2 20T drive pulley                     | 5 mm bore, set screws, for 6 mm GT2 belt, 2-pc pack | 1 pack (2 pcs) | ₹139              | Robu (SKU 52249)          | [Product](https://robu.in/product/aluminum-gt2-timing-pulley-for-6mm-belt-20-tooth-5mm-bore-2pcs/)                                                 |
| 70  | Required | Same       | GT2 toothless idler                      | 20-size smooth, 5 mm bore, 6 mm belt, aluminum, SKU 3963 | 10       | ₹79 × 10 = ₹790   | Flyrobo (SKU 3963)        | [Product](https://www.flyrobo.in/teethless-5mm-inner-hole-2gt-synchronous-pulley-for-6mm-belt)                                                      |
| 4   | Required | Same       | GT2 20T Perlin idler pulley (with teeth) | 5 mm bore, dual bearing, GT2 6 mm belt              | 12             | ₹98 × 12 = ₹1,176 | Robocraze (SKU TIF3P0220) | [Product](https://robocraze.com/products/2gt-20-teeth-pulley-wheel-for-belt-6mm-perlin-passive-idler-pulley-wheel-bore-5mm?variant=43175930691808) |


**Pulleys subtotal:** ₹2,105

## Bearings


| #   | V1       | Mech Ninja | Item                             | Specs                                         | Qty / pack | Price             | Source | Link                                                      |
| --- | -------- | ---------- | -------------------------------- | --------------------------------------------- | ---------- | ----------------- | ------ | --------------------------------------------------------- |
| 24  | Required | Same       | LM10LUU long linear ball bearing | 10 mm ID, 19 mm OD, 55 mm long                | 8          | ₹169 × 8 = ₹1,352 | Novo3D | [Product](https://novo3d.in/lm10luu-linear-ball-bearing/) |
| 3   | Required | Same       | LM8UU linear motion bearing      | 8 mm ID, 15 mm OD, 24 mm long, chromium steel | 12         | ₹37 × 12 = ₹444   | Novo3D | [Product](https://novo3d.in/lm8uu-linear-bearing/)        |


**Bearings subtotal (Required):** ₹1,796

## Aluminum Extrusion 2020


| #   | V1       | Mech Ninja | Item                                | Specs                             | Qty / pack | Price             | Source     | Link                                                                                          |
| --- | -------- | ---------- | ----------------------------------- | --------------------------------- | ---------- | ----------------- | ---------- | --------------------------------------------------------------------------------------------- |
| 27  | Required | Same       | 20×20 mm T-slot aluminium extrusion | 20 × 20 mm, 1 m (1000 mm), T-slot | 8          | ₹480 × 8 = ₹3,840 | OnlyScrews | [Product](https://onlyscrews.in/products/20-20-mm-t-slot-aluminium-extrusion-profile-1-meter) |


**Aluminum Extrusion 2020 subtotal:** ₹3,840

## Nuts and Bolts


| #   | V1       | Mech Ninja          | Item                             | Specs                                      | Qty / pack | Price              | Source     | Link                                                                                                                             |
| --- | -------- | ------------------- | -------------------------------- | ------------------------------------------ | ---------- | ------------------ | ---------- | -------------------------------------------------------------------------------------------------------------------------------- |
| 54  | Required | Same                | M2 × 16 mm socket cap screw      | Grade 12.9 (sub for 15 mm), endstops       | 10         | ₹8.60 × 10 = ₹86   | OnlyScrews | [Product](https://onlyscrews.in/products/m2-x-16mm-hex-allen-socket-head-high-tensile12-9-black-oxide-screw-dia-2mm-length-16mm) |
| 55  | Required | Same                | M2 hex nut                       | SS304                                      | 10         | ₹1.60 × 10 = ₹16   | OnlyScrews | [Product](https://onlyscrews.in/products/m2-nut-ss-304)                                                                          |
| 42  | Required | Same                | M3 × 10 mm socket cap screw      | SS304, DIN 912, 2.5 mm Allen               | 19         | ₹3.20 × 19 = ₹61   | OnlyScrews | [Product](https://onlyscrews.in/products/hex-allen-socket-head-m3-x-10-screw-pack-of-20)                                         |
| 43  | Required | Same                | M3 × 16 mm socket cap screw      | SS304, DIN 912 (sub for 15 mm)             | 22         | ₹3.60 × 22 = ₹79   | OnlyScrews | [Product](https://onlyscrews.in/products/hex-allen-socket-head-m3-x-16-screw-pack-of-20)                                         |
| 44  | Required | Same                | M3 × 20 mm socket cap screw      | SS304, DIN 912, 2.5 mm Allen               | 6          | ₹4.00 × 6 = ₹24    | OnlyScrews | [Product](https://onlyscrews.in/products/hex-allen-socket-head-m3-x-20-screw-pack-of-20)                                         |
| 45  | Required | Same                | M3 × 30 mm socket cap screw      | SS304, DIN 912, 2.5 mm Allen               | 14         | ₹6.00 × 14 = ₹84   | OnlyScrews | [Product](https://onlyscrews.in/products/m3-x-30mm-hex-allen-socket-head-ss-304-screw-dia-3mm-length-30mm)                       |
| 46  | Required | Same                | M3 × 40 mm socket cap screw      | SS304, DIN 912, 2.5 mm Allen               | 12         | ₹12.00 × 12 = ₹144 | OnlyScrews | [Product](https://onlyscrews.in/products/m3-x-40mm-hex-allen-socket-head-ss-304-screw-dia-3mm-length-30mm-din-912)               |
| 47  | Required | Same                | M3 hex nut                       | SS304                                      | 20         | ₹0.90 × 20 = ₹18   | OnlyScrews | [Product](https://onlyscrews.in/products/m3-nut-ss-304)                                                                          |
| 48  | Required | They have, we don't | M3 hex nut (square-nut stand-in) | SS304; M3 square not sold here             | 13         | ₹0.90 × 13 = ₹12   | OnlyScrews | [Product](https://onlyscrews.in/products/m3-nut-ss-304)                                                                          |
| 52  | Required | Same                | M4 × 40 mm socket cap screw      | SS304, bed corners                         | 4          | ₹7.60 × 4 = ₹30    | OnlyScrews | [Product](https://onlyscrews.in/products/m4-x-40mm-hex-allen-socket-head-ss-304-screw-dia-4mm-length-40mm)                       |
| 53  | Required | Same                | M4 hex nut                       | SS304                                      | 4          | ₹1.20 × 4 = ₹5     | OnlyScrews | [Product](https://onlyscrews.in/products/m4-nut-ss-304)                                                                          |
| 49  | Required | Same                | M5 × 8 mm button-head screw      | Grade 10.9 black oxide (SS304 button OOS)  | 68         | ₹2.80 × 68 = ₹190  | OnlyScrews | [Product](https://onlyscrews.in/products/m5-x-8mm-hex-allen-button-head-high-tensile10-9-black-oxide-screw-dia-5mm-length-8mm)   |
| 50  | Required | Same                | M5 × 20 mm button-head screw     | SS304, 3 mm Allen                          | 18         | ₹3.80 × 18 = ₹68   | OnlyScrews | [Product](https://onlyscrews.in/products/hex-allen-button-head-m5-x-20-screw-pack-of-20)                                         |
| 51  | Required | Same                | M5 hex nut                       | SS304                                      | 2          | ₹1.40 × 2 = ₹3     | OnlyScrews | [Product](https://onlyscrews.in/products/m5-nut-ss-304)                                                                          |
| 28  | Required | Same                | M5 hammer T-nut, 2020 series     | M5, nickel, 6 mm slot, drop-in, SKU C7 010 | 70         | ₹5.50 × 70 = ₹385  | Novo3D     | [Product](https://novo3d.in/hammer-nut/?attribute_type=2020&attribute_size=M5)                                                   |
**Nuts and Bolts subtotal:** ₹1,205

## Print files


| #   | V1       | Mech Ninja          | Item                               | Specs                                                                | Qty / pack | Price | Source                            | Link                                                                  |
| --- | -------- | ------------------- | ---------------------------------- | -------------------------------------------------------------------- | ---------- | ----- | --------------------------------- | --------------------------------------------------------------------- |
| 41  | Required | They have, we don't | Mech Ninja DIY CoreXY STL + manual | Digital: STLs, BOM.xlsx, assembly/wiring PDF                         | 1          | TBD   | Cults (TheMechNinja)              | [Files](https://cults3d.com/pt/modelo-3d/diversos/diy-corexy-printer) |
| 38  | Required | Better than theirs | CoreXY X carriage / toolhead       | Bolt-on mount for BMG + V6 + 4010 radial fan + probe; belt clamps; not zip ties | 1          | TBD   | Included in item 40 service print | —                                                                     |
**Print files subtotal:** TBD

## Optional

Not on the Mech Ninja list, plus spares and V2. Not part of the required buy.


| #   | V1       | Mech Ninja          | Item                               | Specs                                                         | Qty / pack       | Price          | Source                    | Link                                                                                                                                     |
| --- | -------- | ------------------- | ---------------------------------- | ------------------------------------------------------------- | ---------------- | -------------- | ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| 67  | Optional | We have, they don't | IEC power entry, switch and fuse holder | Pack of 2, male C14, 250 V AC, 15 A, snap-in, red, 5×20 mm fuse not included, ASIN B09VPL265H | 1 pack | ₹151 | Amazon | [Product](https://www.amazon.in/dp/B09VPL265H) |
| 68  | Optional | We have, they don't | Earth wire | Green/yellow, 1.5 mm². IEC earth pin → both PSU cases → 2020 frame | 1 m | TBD | Local market | — |
| 66  | Optional | We have, they don't | Insulated wire ferrule kit | 1200 pcs, bootlace pin ferrules, 0.5–10 mm² (AWG 22–7), 8 sizes, ASIN B0CJ2Q4MSP | 1 pack | ₹449 | Amazon | [Product](https://www.amazon.in/dp/B0CJ2Q4MSP) |
| 57  | Optional | We have, they don't | HIKVISION Extreme microSD | 8 GB, Class 10, ASIN B0GVJRTL4D | 1 | ₹379 | Amazon | [Product](https://www.amazon.in/dp/B0GVJRTL4D) |
| 58  | Optional | We have, they don't | XT-02 microSD to SD adapter | Full-size SD shell for item 17 slot, pack of 1 | 1 | ₹134 | Amazon | [Product](https://www.amazon.in/dp/B0F3266YN1) |
| 21  | Optional | We have, they don't | MKS MOS25 V1.0 MOSFET heater module | 12/24 V, 25 A / 300 W max | 1 | ₹179 | Robocraze (SKU TIF3P0134) | [Product](https://robocraze.com/products/3d-printer-parts-heating-controller-mks-mos25-v1-0-for-heat-bed-extruder-mos-module-support-big-current-25a?variant=42970566688992) |
| 63  | Optional | We have, they don't | High-current bed wiring | 16 AWG (1.5 mm²) silicone, red and black, bed supply → MOS25 → bed | 2 m | TBD | Local market | — |
| 65  | Optional | We have, they don't | Thermistor wire | 24 AWG twisted pair, hotend sensor → Gen-L. Keep off the heater pair | 2 m | TBD | Local market | — |
| 64  | Optional | We have, they don't | 24 V wiring | Silicone, red and black. 16 AWG ~1 m logic supply → Gen-L; 20 AWG ~2 m V6 heater and 24 V fans | 1 shop buy | TBD | Local market | — |
| 22  | Optional | We have, they don't | 4-start T-type copper nut | 8 mm screw, 2 mm pitch / 8 mm lead | 4 | ₹63 × 4 = ₹252 | Robocraze (SKU TIF3P0014) | [Product](https://robocraze.com/products/4-start-t-type-copper-nut-2mm-pitch?variant=40193520599193) |
| 39  | Optional | We have, they don't | Bowden PTFE tube | 4 mm OD / 2 mm ID, 1.75 mm filament | 1 m | TBD | Send listing | — |
| 69  | Optional | We have, they don't | M3 / M4 / M5 hex nut and washer pack | SS304. 50 nuts + 50 washers of each size. Variant 49537778614585 | 1 pack | ₹470 | OnlyScrews | [Product](https://onlyscrews.in/products/hex-nuts-and-washers-assorted-screw-pack-m3-m4-m5-ss304?variant=49537778614585) |
| 40  | Optional | We have, they don't | Outsourced CAD print job | Selected prints from item 41 (compatible mounts only), PETG/ABS | 1 job | TBD | Other printer or print service | — |
| 61  | Optional | We have, they don't | XSOURCE PLA 1.75 mm | 1 kg spool, ±0.03 mm, yellow, ASIN B0F2J38K8H | 1 | ₹598 | Amazon | [Product](https://www.amazon.in/dp/B0F2J38K8H) |
| 73  | Optional | We have, they don't | Bed leveling screw, spring and knob | M3 × 40 mm screw, spring, knob. Pack of 4. Silver. ASIN B07K1X6RDV | 1 pack (4) | ₹299 | Amazon | [Product](https://www.amazon.in/dp/B07K1X6RDV) |
| 11  | Optional | They have, we don't | 608-2RS rubber-sealed ball bearing | 8 × 22 × 7 mm                                                 | 1 pack (10 pcs)  | ₹206           | Meesho                    | [Product](https://www.meesho.com/608-2rs-10pics-rubber-sealed-ball-bearings-8x22x7mm-for-3d-printer-robotics-ii-608-2rs-10-pcs/p/93lnru) |
| 25  | Optional | We have, they don't | SK10 shaft support                 | 10 mm, 1 pc. Printed supports are on hand                    | 8                | ₹65 × 8 = ₹520 | Novo3D                    | [Product](https://novo3d.in/sk10-10mm-linear-bearing/)                                                             |
| 26  | Optional | We have, they don't | SK8 shaft support                  | 8 mm, 1 pc. Printed supports are on hand                     | 4                | ₹59 × 4 = ₹236 | Novo3D                    | [Product](https://novo3d.in/product/sk8-8mm-linear-bearing-rail/)                                                  |
| 19  | Optional | They have, we don't | NTC MF52 100K 3950 thermistor 1%   | Bead type, pack of 5                                          | 1 pack (5 pcs)   | ₹39            | Robu (SKU 1308091)        | [Product](https://robu.in/product/ntc-mf52-100k-ohm-3950-thermistor-1-pack-of-5/)                                                        |
| 20  | Optional | We have, they don't | HT-NTC100K thermistor, 2 m lead    | Stainless probe, high-temp cable                              | 1                | ₹103           | Robocraze (SKU TIF3P0104) | [Product](https://robocraze.com/products/thermistor-temperature-sensor-ht-ntc100k-2m?variant=40194370142361)                             |
| 7   | Optional | We have, they don't | White nylon cable ties             | 4 / 6 / 8 / 10 inch mix, natural colour                       | 1 pack (400 pcs) | ₹152           | Meesho                    | [Product](https://www.meesho.com/white-nylon-cable-tie-4-6-8-and-10-inch-super-strong-natural-colour-400-pcs-free-tester/p/gtyf74)       |
| 31  | Optional | We have, they don't | Auto bed probe                     | CRTouch / BLTouch, 3-wire servo + 5 V                         | 1                | TBD            | Send listing              | —                                                                                                                                        |
| 32  | Optional | We have, they don't | 32-bit printer board               | SKR / Octopus class, 24 V, 5+ drivers                         | 1                | TBD            | Send listing              | —                                                                                                                                        |
| 33  | Optional | We have, they don't | Klipper host                       | Raspberry Pi or CB1                                           | 1                | TBD            | Send listing              | —                                                                                                                                        |
| 34  | Optional | We have, they don't | ADXL345 accelerometer              | Input shaper, USB or SPI                                      | 1                | TBD            | Send listing              | —                                                                                                                                        |
| 35  | Optional | We have, they don't | Switching PSU (V2)                 | 24 V 20–25 A (480–600 W)                                      | 1                | TBD            | Send listing              | —                                                                                                                                        |
| 36  | Optional | We have, they don't | MGN12 linear rail + carriage       | ~300–400 mm, XY (length after CAD)                            | 4                | TBD            | Send listing              | —                                                                                                                                        |
| 37  | Optional | We have, they don't | High-flow hotend                   | CHT / Dragon class, 24 V, 1.75 mm                             | 1                | TBD            | Send listing              | —                                                                                                                                        |


**Optional subtotal:** ₹4,167 (items 39, 40, 63, 64, 65, 68, and 31–37 not priced)

Notes:

- PVC pipe, elbows, Tees, and crosses were removed. The frame is **2020** (item 27) with corners (29) and T-nuts (28).
- Item 1 replaced the M8 × 1.25 threaded rods and brass T-nuts. Two 1000 mm T8 **4-start** screws (2 mm pitch → **8 mm lead**), each with a copper nut. Cut them into **three** Z screws. 2000 mm covers three screws as long as each is under about 650 mm. The third nut comes from item 22. A full-length 1000 mm screw will bend. Marlin/Klipper Z: 200 × 16 / 8 = **400 steps/mm**, then calibrate.
- Item 22 matches item 1 (4-start, 8 mm lead) and is optional, because Mech Ninja does not list extra nuts. Put one extra nut on each screw, sprung against the drive nut, and keep two as spares. Each screw still needs a light compression spring over the 8 mm thread. Do not mix with old M8 × 1.25 nuts.
- Item 2 replaced Robu 4.2 kg-cm (~1.2 A). Novo3D **4.8 kg-cm, 2 A, 47 mm** body, attached cable. Set TMC2209 current for 2 A (not the 1.25 A default) and keep heatsinks. Checkout: **Attached cable** (SKU G4 006, ₹609), not detachable (₹769).
- Item 3 is Novo3D LM8UU (₹37). These fit 8 mm smooth rods, not the lead screws.
- Item 4 replaced the 16T / 3 mm Perlin. These are 20T / 5 mm dual-bearing **toothed** idlers (M5 bolt). Do not use them on the smooth back of the belt. Keep them for a bend that actually wraps the tooth side, or as spares. Idler tooth count does not change steps/mm.
- Item 5 replaced the 16T drive. This is a **2-pc drive pack** (set screws, not bearings). These are the only toothed pulleys on the motors. 20T × 2 mm pitch → XY **80 steps/mm** (was 100). Items 4, 5, 9, and 70 all use 6 mm GT2.
- Item 70 is the bend idler: toothless, 20-size, 5 mm bore, **6 mm** belt, SKU 3963. Qty **10** uses the 10+ price (₹79; singles are ₹85). The smooth back of the belt rides here. Confirm the bore has a bearing and the wheel has side flanges before checkout. The page has shown both in stock and an out-of-stock notice.
- Item 9 is Novo3D steel-core, 500 cm (5 m) × 2 (₹0.69/cm + GST). Novo3D ships multiple lengths as one roll unless you order separately.
- Item 6 (8 mm smooth rods) matches the LM8UU bearings. Qty is 2 packs = 4 rods. Cut to axis length; leftovers can guide Z. Do not use lead screws as linear guides.
- Item 8 couples a NEMA17 5 mm shaft to the 8 mm lead screws (item 1). Three couplings match the three screws.
- Item 10 replaced the MK8 kit. BMG dual-gear, unassembled, mounts on a NEMA17. Pairs with the V6 hotend (item 13).
- Item 13: Kingroon V6 24 V 40 W. Item 60 is the **E3DV6 Black Regular** sock for that block. Checkout Type **E3DV6 Black Regular** (₹18), not PT100 / Volcano / MK8.
- Item 11 is a rotary 608 bearing (idlers/spools/wheels), not a linear substitute for the LM8UU.
- Item 12 replaced the 235 mm Neptune plate. Novo3D **310 × 310 × 3 mm** aluminium, **24 V**, **220 W** (~9.2 A), 100 cm cable, SKU D3 007, ₹1,799, in stock. The cable version includes an NTC 100K thermistor and JST housings. The wires arrive unsoldered and uncrimped. Mounting holes are 4 mm and countersunk, so the bed corners are the M4 × 40 screws (items 52 and 53). One item 14 supply feeds it, through MOS25 (item 21) if that module is bought. Side margin in the 480 mm opening is (480 − 310) / 2 = **85 mm**.
- Item 74 is the build surface on item 12: Two Trees **310 × 310 mm** double-sided textured PEI with a magnetic base, SKU 1645137, ₹1,899, in stock. Stick the magnet to the aluminium. The spring sheet is the print surface. It stays required because this bed has no PEI of its own.
- Item 73 is four bed-leveling sets: **M3 × 40 mm** screw, spring, and knob, ₹299. The heater holes are **4 mm**, so these M3 screws are loose in them. Use items 52 and 53 for the corners unless the holes are checked and are actually M3.
- Item 14 qty **2**. Both are 24 V and match the V6 (item 13) and the Gen-L (12–24 V). Set each input switch to 220 V for India. Split the loads: one supply → MOS25 → bed only; the other → Gen-L, hotend, motors, and fans. Tie the two DC negatives together so the MOS25 control signal has a reference. Do not tie the two DC positives together.
- Item 2 is **6** motors: X, Y, extruder, and three Z. Item 15 stays at **5** TMC2209s because the Gen-L has five sockets. Two Z motors share one driver, wired in parallel with the same coil order. Those motors are 2 A each, and one TMC2209 cannot give both of them 2 A, so that pair has less torque than the single Z motor. Set the shared driver's current so the chip stays inside its limit. UART/sensorless needs firmware setup.
- Item 16 replaced RAMPS 1.4 + Mega 2560 with one MKS Gen-L board.
- Item 17 replaced the bare 12864 module. This kit includes the smart adapter, encoder, and **full-size SD** slot. It is made for RAMPS/Gen-L EXP headers. Item 57 is the microSD; item 58 is the plastic adapter so it fits that slot. Format **FAT32**. 8 GB is enough for gcode. Do not buy the Amazon extended-warranty add-on.
- Item 18: 5 mechanical endstops (was 3). Typical use: X min, Y min, Z min, plus two extras (second Z, Y max, or spares). Wire COM + NO/NC to the Gen-L endstop headers (usually 5 V).
- Item 19 is one pack of 5 bead thermistors (100K 3950). Typical Marlin type 1 or 5. Use on the V6 if the kit thermistor is missing/wrong.
- Item 20 is the 2 m stainless-probe sensor. Use it only if the item 12 thermistor is missing or the wrong table. The cable version includes an NTC 100K. Confirm 100K vs 10K before firmware.
- Item 21 is optional. If you buy it, run the bed supply (one item 14) → MOS25 → bed, PWM from the Gen-L bed pin. Stay under 25 A and give the module cooling. The bed supply sees ~9.2 A of its 15 A rating.
- Item 63 is the high-current bed run, bought locally. **16 AWG (1.5 mm²) silicone**, red and black, about 2 m: bed supply → MOS25 → bed. Ferrule the screw terminals. This is not the hotend, thermistor, or endstop wire.
- Item 64 is the other **24 V** silicone, also local. About 1 m of 16 AWG for the logic supply → Gen-L, and about 2 m of 20 AWG for the V6 heater extension and the 24 V fans (items 30 and 56). Red and black. Endstop wire is still separate.
- Item 65 is the thermistor lead, bought locally. **24 AWG twisted pair**, about 2 m, from the hotend sensor to the Gen-L. Route it away from item 64. The bed thermistor comes with the 100 cm cable. Extend it with the same wire only if that tail is cut short.
- Item 66 is a 1200-pc insulated **bootlace ferrule** kit, AWG 22–7 (0.5–10 mm²), ₹449. Use these on items 63 and 64 where they land in screw terminals (PSU, MOS25, Gen-L). The listing is ferrules only, so the crimp still needs pliers. This kit is not Dupont housings for endstops and fans.
- Item 67 is one pack of **2** IEC inlets with a rocker switch and a 5×20 mm fuse drawer, ₹151. Use one; keep the second as a spare. The fuse is **not** in the pack. Fit a **5 A slow-blow 5×20 mm** fuse: both item 14 supplies share this inlet, and a 15 A fuse would not protect the mains wire. Earth conductor is item 68. Live and neutral still need a short mains lead from the module to the two PSU inputs. Snap-in mount needs a panel cutout.
- Item 68 is the **earth wire**, bought locally. Green/yellow, **1.5 mm²**, about 1 m: IEC earth pin → both PSU earth screws → one point on the 2020 frame (M5 T-nut). Use ring terminals on the screws. This is not the red/black 24 V wire.
- Item 23 is **10 mm** and does **not** fit LM8UU (item 3). Qty 2 × 1000 mm = four XY cuts (**480–500 mm**), one cut per bar. That length matches the 520 mm outer frame. Do not cut these rods for a 300 mm box. Confirm stock.
- Item 24: 8 × LM10LUU for XY (2 per 10 mm rod). Keep LM8UU (item 3) for Z guides on leftover 8 mm rod until MGN12 (item 36).
- Item 25: SK10 × 8 would be 4 × 10 mm XY rods × 2 ends. Printed supports are already on hand, so this row is optional. If a printed block cracks, the Novo3D part bolts to 2020 with M5 T-nuts (28).
- Item 26: SK8 × 4 would be 2 × 8 mm Z guide rods × 2 ends. Printed supports are already on hand, so this row is optional. Not for 10 mm rods.
- Item 27 is the frame: 8 × 1000 mm of 20×20 (8000 mm). That builds the **520 mm** outer box once: eight 480 mm XY rails, one 480 mm gantry, and four posts from the remaining 3680 mm. It cannot be cut into a 300 mm cube and then recut. Listing showed **sold out / low stock** — confirm before checkout. Do not cut until CAD is frozen.
- Items 38–41 are unpriced until you send listings (item 29 is now priced). First bring-up can stay Gen-L + V6 + 360 W + LUU; do not buy 32–37 for that smoke test.
- Item 28 is **2020 / M5** (in stock). Qty **70** matches Mech Ninja. Checkout: Type **2020**, Size **M5**.
- Items 42–55 are the Mech Ninja fastener list from OnlyScrews (Novo3D kits are too short on M5×8). **M3 × 15 mm Allen does not exist** there → item 43 is **16 mm**. **M2 × 15 mm** does not exist → item 54 is **16 mm**. **M3 square nut** is not sold on OnlyScrews or Novo3D (they have M5/M6 square only) → item 48 is extra M3 hex; if a printed pocket is truly square, catch a hex or buy square locally. SS304 **M5 × 8 button is out of stock** → item 49 is 10.9 black-oxide button (correct head for 2020 T-nuts). Socket-cap M5×8 SS304 is in stock if you prefer: [listing](https://onlyscrews.in/products/hex-allen-socket-head-m5-x-8-screw-pack-of-20) ₹4. Item 52/53 are M4 × 40 for the 4 mm countersunk bed corners. Flat washers are item 69.
- Item 29: Novo3D 2020 3-way × 8 = 8 corners of a closed 2020 box. Checkout **Type: 2020** (₹89); do not pick 3030/4040. Qty 6–10 is ~2% off at checkout. Confirm grub screws/lock nuts in the pack.
- Item 59: Mech Ninja interior **L-shape 90°**. Novo3D 2020, ₹45, M4 grub. Qty **4** for now. Confirm screws in the pack. This is not a three-way cube and not an external corner bracket.
- Item 71: Novo3D **L-type** 2020 connector, ₹55, qty **10**. This is the external corner plate, not the interior L (item 59) and not the three-way cube (item 29). The 20+ price is about 3% off; ten stays at ₹55. In stock.
- Item 69 is one OnlyScrews SS304 assortment, ₹470: **50 hex nuts and 50 flat washers** each of M3, M4, and M5. These are plain hex nuts, not M5 locknuts, so idler bolts still want nylocs. The product page showed **sold out / low stock** — confirm before checkout.
- Item 56: two **24 V** 4010s, Required, SKU TIF3P0180, ₹69 each. One on the MOS25 / Gen-L / TMC heatsinks, one spare or on the V6 heatsink if the kit fan dies. **Not** part cooling. 0.09 A, ~22 cm cable. Wire to a 24 V fan header or always-on 24 V. The 5 V 4010s were removed.
- Item 30 is the Mech Ninja layer fan: TESSERACT **4010 radial** blower, 24 V, 0.07 A, 1.6 CFM, ₹325, ASIN B08QJMZC71. Checkout size **4010 24V Radial Fan**, not the 12 V sizes. It bolts to item 38. This is part cooling. Item 56 is the axial 4010 and is not a substitute.
- Item 31: probe for mesh / Z-offset. Keep mechanical endstops (item 18) for XY. 5 V logic on Gen-L; confirm 5 V vs 24 V probe.
- Item 32: replaces Gen-L (item 16) for Klipper speed, not for the first Marlin bring-up. Keep item 16. TMC2209s (item 15) can move over if the new board is STEP/DIR.
- Item 33: Klipper host. Not needed on Marlin/Gen-L.
- Item 34: Input shaper after Klipper is running. Useless on stock Marlin/Gen-L.
- Item 35: single-box V2 replacement for the two item 14 supplies. Not needed for first prints if those two stay split. Do not parallel any two 24 V positives onto one rail.
- Item 36: 4× MGN12 for XY (2 per axis typical). Length after CAD (~300–400 mm). Replaces LM10LUU (item 24) later. Buy rail+carriage sets, not rails alone.
- Item 37: V2 hotend. Keep V6 (item 13) for first extrusion tests. BMG (item 10) stays.
- Item 38: the actual toolhead. Holds BMG (10), V6 (13), the 4010 radial fan (30), probe (31), and GT2 belt ends. Not the Mech Ninja MK8 STL. Print with item 40 after a small CAD pass. Zip ties stay for cable dressing only.
- Item 39: short PTFE from BMG into the V6. Direct-drive; not a long Bowden.
- Item 40: **one outsourced print job** on another machine or a service. Source files are item 41. Print only parts that match this BOM (2020 motor/idler blocks, belt path, and a carrier for the 310 mm plate). Do not print M8 nut blocks or the MK8 toolhead. The bed mounts must match item 12’s 4 mm countersunk holes, not a 235 mm Neptune pattern. PETG/ABS for load parts. Send the service quote to price this row.
- Item 41: Mech Ninja **files**, not their hardware kit. Cults is about **US$9** (confirm at checkout). STLs + BOM.xlsx + assembly/wiring manual. Buy this before item 40. Wiring PDF is RAMPS-oriented — use it as a map, not as Gen-L gospel. Aluminum corners (item 29) replace their printed corner cubes; do not print both.
- Item 61: 1 kg **1.75 mm PLA** spool for first prints. Colour is only yellow. Few Amazon reviews. Dry if it prints stringy. Load parts (item 40) stay PETG/ABS.



## Total


| Category                | Priced      | TBD                        |
| ----------------------- | ----------- | -------------------------- |
| Electronics (Required)  | ₹17,932     | —                          |
| Hardware (Required)     | ₹5,540      | —                          |
| Pulleys                 | ₹2,105      | —                          |
| Bearings (Required)     | ₹1,796      | —                          |
| Aluminum Extrusion 2020 | ₹3,840      | —                          |
| Nuts and Bolts          | ₹1,205      | —                          |
| Print files             | —           | 38, 41                     |
| **Required subtotal**   | **₹32,418** | 38, 41                     |
| Optional                | ₹4,167      | 39, 40, 63, 64, 65, 68, 31, 32, 33, 34, 35, 36, 37 |


**Grand total (priced items):** ₹36,585
**V1 Required only (priced):** ₹32,418

Unpriced rows are not included. Shipping, GST at checkout, and cut-to-length waste are extra.