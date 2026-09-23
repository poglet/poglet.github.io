---
layout: default
title: Learning to Solder
description: A growing collection of soldering resources for beginners, including a shopping list of gear, tutorial videos, and starter project ideas.
parent: Guides
grand_parent: Home
nav_enabled: true
---

# Learning to Solder: Beginner's Guide and Resources

A growing collection of soldering resources for beginners, including a shopping list of gear, tutorial videos, and starter project ideas. This page collects what I have found useful while teaching myself to solder for retro hardware repairs.

---

## Shopping List

### Essential Gear

* **Soldering iron or soldering station** — a temperature-controlled station in the 60W+ range is much easier to learn with than a cheap fixed-heat pencil iron. Look for one with easily replaceable tips (chisel tips around 2–3mm cover most through-hole work).
* **Solder wire** — 0.5–0.8mm diameter, rosin core. Leaded 60/40 or 63/37 is the easiest to learn with (wash your hands after use); lead-free is the modern standard but needs higher temperatures and is less forgiving.
* **Brass tip cleaner or wet sponge** — keeps the tip clean and tinned. A brass wool cleaner is less thermally shocking than a wet sponge.
* **Solder sucker (desoldering pump)** — for undoing mistakes and removing through-hole components.
* **Desoldering braid (solder wick)** — complements the sucker and is essential for cleaning up pads.
* **Flux pen or paste** — makes solder flow properly and fixes most wetting problems on older joints.
* **Helping hands or a PCB holder** — holds the board steady so you can focus on technique.
* **Flush cutters** — for trimming component leads after soldering.
* **Safety glasses** — flux can spit and leads can fly when clipped.

### Nice to Have

* **Fume extractor or desk fan** — keeps flux fumes away from your face.
* **Magnifying glass or loupe** — helps inspect joints for bridges and cold solder.
* **Hot air rework station** — only needed later for surface-mount work and removing multi-pin chips.
* **Multimeter** — useful for continuity checks and verifying repairs before powering on.

---

## Videos to Watch

* **[EEVblog #180 — Soldering Tutorial Part 1](https://www.youtube.com/watch?v=fYz5nIHH0iY)** — the classic beginner tutorial on through-hole soldering technique. Start here.
* **[EEVblog #183 — Soldering Tutorial Part 2 (Surface Mount)](https://www.youtube.com/watch?v=M2Jf9ce2QFc)** — a follow-up covering surface-mount soldering basics.
* **[How to Solder Correctly — Adafruit](https://www.youtube.com/watch?v=fJm6y1c0s3I)** — a short, clear demonstration of good joint technique.
* **[Collin's Lab: Soldering — Adafruit](https://learn.adafruit.com/collins-lab-soldering)** — companion written guide with close-up photos.
* **[Retro Repairs soldering streams](https://www.youtube.com/results?search_query=retro+computer+recapping)** — watch experienced repairers recap old motherboards; great for seeing real-world repairs.

---

## Projects

### Beginner Projects

* **LED blinky kits** — cheap "learn to solder" kits with a handful of resistors and LEDs. Perfect first boards; practice heating the pad and the lead together.
* **555 timer circuits** — small kits that produce sound or flashing patterns. A good step up from LEDs.
* **Practice PCB kits** — blank practice boards sold purely for repetition. Great for building muscle memory without risking real gear.

### Intermediate Projects

* **Recap an old motherboard** — replacing bulging or leaking capacitors is a rite of passage in retro computing. Start on dead boards before touching hardware you care about. Machines like the one in [My Old Computer]({% link home/guides/my-old-computer.md %}) often need exactly this work.
* **Replace a broken DC jack** — a very common laptop and console repair that is easier than it looks.
* **Wire up a Raspberry Pi or Arduino project** — headers, buttons, and LEDs on perfboard.

### Longer-Term Projects

* **Keyboard or controller mods** — swapping switches or installing LEDs in game controllers.
* **Repairing retro expansion cards** — Sound Blaster, network cards, and video cards from the Socket A era often just need new capacitors. Pair the repair with the software setup in [Various Methods for Running Windows 98]({% link home/guides/various-methods-for-running-windows-98.md %}).

---

## Related Guides

* [My Old Computer]({% link home/guides/my-old-computer.md %}) — restoring an AMD Sempron 2500+ PC, including hardware that may need soldering work.
* [Various Methods for Running Windows 98]({% link home/guides/various-methods-for-running-windows-98.md %}) — what to install once the hardware is repaired.
