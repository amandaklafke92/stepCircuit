# Anklet prototype options — initial research

Researched 17 September 2026. Amanda is leaning towards an anklet; this is a preference to explore, not a final form-factor decision. No parts selected or purchased.

## What the evidence supports

Ankle placement is a credible direction for step counting. A 2018 study comparing wrist and ankle sensors under four treadmill conditions found better performance at the ankle for the algorithms tested. This supports investigating ankle placement; it does not validate our future device, loose jewellery, or everyday accuracy. [Rhudy and Mahoney, 2018](https://pubmed.ncbi.nlm.nih.gov/29846134/)

The CADENCE-adults study also reported favourable results for ankle-worn devices at normal treadmill speeds. Hardware, algorithms, and placement varied together, so its error figures should not become promises for StepCircuit. [CADENCE-adults, 2022](https://pubmed.ncbi.nlm.nih.gov/36076265/)

## Physical design options

These are design hypotheses, not experimentally verified rankings.

| Option | Advantage | Trade-off to test |
|---|---|---|
| Removable enclosed module on an adjustable soft ankle strap | Allows repeatable positioning and easy enclosure changes | More like a fitness accessory than jewellery; comfort with socks and shoes needs testing |
| Integrated centrepiece on a fitted jewellery-style anklet | Closer to the desired finished object; two attachment points could limit swinging | Rotation, fit, clasp security, weight, and actual component volume need testing |
| Freely dangling electronic charm | Familiar jewellery format | Adds independent swinging and impacts; likely harder to interpret movement consistently |

Agent recommendation: test a removable module on a soft strap first, with an integrated jewellery centrepiece as a candidate next enclosure. Amanda has not selected this route. A non-electronic size-and-fit mock-up could precede buying electronics.

## Two illustrative electronics routes

A development board is a ready-made circuit board containing the small computer and supporting electronics. These two candidates also include motion sensing and Bluetooth, reducing the amount we would need to wire ourselves.

| Candidate | Verified properties | Implication for this experiment |
|---|---|---|
| Seeed XIAO nRF52840 Sense, original model | 21 × 17.8 mm board footprint; Bluetooth, accelerometer/gyroscope, USB-C, battery charging; battery solder pads | More promising for a small wearable, but battery connection requires soldering or a suitable adapter |
| Adafruit Feather nRF52840 Sense | 51 × 23 × 7.2 mm without headers; Bluetooth, motion sensors, USB and charging; plug-in battery connector | Easier battery assembly with a correctly matched battery, but substantially larger |

Sources: [Seeed documentation](https://wiki.seeedstudio.com/XIAO_BLE/), [Adafruit product specifications](https://www.adafruit.com/product/4516), [Adafruit power guide](https://learn.adafruit.com/adafruit-feather-sense/power-management).

Dimensions above are for the boards, not finished products. Battery, protective case, attachment points, and access for charging add volume. No complete dimensions or runtime estimate is justified yet. The smaller board is not automatically the easier beginner option.

Before selecting a battery, verify its permitted charging current, protection, polarity, and connector against the exact board revision. Seeed's documentation includes charging-control and battery-reading caveats that require checking before implementation; do not copy example code uncritically. The initial wearable would need an enclosure protecting the battery and electronics; no water-resistance claim has been established.

## iPhone feasibility test

We can test Bluetooth data transfer using Nordic's existing nRF Connect app on iPhone before writing a companion app. It can inspect and communicate with Bluetooth Low Energy devices; it is a diagnostic interface, not the finished step dashboard or automatic Google Sheets integration. [Nordic's iOS testing instructions](https://academy.nordicsemi.com/courses/bluetooth-low-energy-fundamentals/lessons/lesson-1-bluetooth-low-energy-introduction/topic/blefund-lesson-1-exercise-1/?version=v3.4.0)

## Candidate experiments for discussion

1. Wear dummy modules representing plausible board-plus-battery volumes on an adjustable strap. Observe fit, rotation, security, and contact with footwear. Exact dummy dimensions should follow a proposed battery layout, not board dimensions alone.
2. Capture motion data from a real ankle-worn prototype and compare counts with manually counted walking at different speeds, starts/stops, and stairs. Include seated foot tapping and other non-walking movements. Use Oura as a comparison, not ground truth.
3. Check Bluetooth transfer from ankle to iPhone and measure power use before projecting battery life.

These are proposed experiments, not agreed acceptance criteria or a build order. Blender assembly instructions should follow selected parts and actual connections; a render cannot establish electrical correctness.

## What would narrow the choice

- Does Amanda imagine a fine chain, a fitted decorative band, or a soft discreet strap?
- Would a bulkier temporary strap be acceptable for learning before making the jewellery enclosure?
- Is learning a little soldering appealing, or should the first assembly prioritise plug-in connections?
- What budget, charging frequency, wear conditions, and degree of visibility would be acceptable?

## Process lesson

We are exploring options and separating uncertainties: electronics feasibility, counting performance, and jewellery comfort are different questions. They can use different prototypes. Research narrows the options; physical tests establish whether the option works for Amanda.
