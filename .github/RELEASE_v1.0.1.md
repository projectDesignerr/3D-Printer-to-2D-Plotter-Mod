# 3D Printer to 2D Pen Plotter v1.0.1

## What's New in v1.0.1
- 🐛 Several bugs fixed
- 🆕 PCB feature added
- 📜 **Apache 2.0 License added** - Full legal clarity on how you can use this project

## 📜 License Information

This release is now licensed under **Apache License 2.0**.

### What You Can Do:
✅ Use the code for personal or commercial projects
✅ Modify and adapt the code to your needs
✅ Distribute the code or your modifications
✅ Use it in proprietary applications

### What You Must Do:
📋 Include a copy of the Apache 2.0 license with any distribution
📝 State changes - clearly document any modifications you make
✏️ Keep the original copyright notice and attribution
⚖️ Accept that this software is provided "AS-IS" with NO WARRANTY

**Full License:** See [LICENSE](../LICENSE) file in the repository

---

## Installation & Quick Start

1. Download **`GCodePlotter_v1.0.1_Windows_x64.zip`** from Assets
2. Extract the folder anywhere on your PC
3. Double-click **`GCodePlotter.exe`**
4. Configure your printer settings and start plotting!

## ⚠️ Critical Safety Note

**DO NOT insert the pen before homing!** During auto-homing, your printer will drive the nozzle down. If the pen is already mounted lower than the nozzle, it will crash and break.

**Safe procedure:**
1. Remove or raise the pen from the holder
2. Start the print - printer will perform auto-home
3. Insert and clamp your pen while printhead is elevated
4. Machine will safely lower the pen and begin plotting

---

## 📐 Bed Calibration & Pen Mounting Guide

### ⚠️ CRITICAL: Pen Removal Before Bed Leveling

> **IMPORTANT:** You **MUST UNMOUNT THE PEN** before performing bed leveling (bed mesh probing, ABL, or manual bed leveling). After leveling is complete, **MOUNT THE PEN AGAIN** for drawing operations.

**Why?** Bed leveling sensors need to touch the bed surface at the nozzle height. If the pen is mounted, it will interfere with the probe and cause incorrect calibration.

### Step-by-Step Calibration Process

#### 1. **UNMOUNT PEN** - Before Any Bed Leveling
   - Remove the pen from the holder completely
   - Raise the toolhead to a safe height
   - This allows your printer's bed mesh/ABL probe to work correctly

#### 2. **Perform Bed Leveling/Mesh Probing**
   - Run your printer's normal bed leveling routine (G29, G28, etc.)
   - This establishes the correct nozzle-to-bed distance
   - Do NOT have the pen mounted during this step

#### 3. **MOUNT PEN AGAIN** - After Bed Leveling Complete
   - Once bed leveling is finished and approved
   - Install your pen into the bracket/holder
   - Clamp it securely in place
   - Now ready for drawing operations

#### 4. **Finding Your Pen Touch Z Height**
   1. Place paper/notebook on the bed
   2. Using your printer's control, jog the Z-axis down slowly (0.1 mm increments)
   3. Stop when the pen tip **just touches the paper** with gentle pressure
   4. Note the Z coordinate (e.g., `9.40 mm`)
   5. Enter this value into **Pen Touch Z (mm)** in the app
   6. Set **Z-Hop (mm)** to `3.0 mm` (height lifted between strokes)

#### 5. **Finding Toolhead Mount Offsets (X / Y Offsets)**
   If your pen is mounted to the side or front of your extruder nozzle:
   1. Jog your printer until the **pen tip** is at corner (0, 0)
   2. Read the coordinates on your printer screen
   3. **X Offset:** Difference in X position from nozzle
   4. **Y Offset:** Difference in Y position from nozzle
   5. Enter these into **Offset X** and **Offset Y** fields in the app

#### 6. **Notebook / Ruled Page Alignment** (Optional)
   - **Enable Notebook Mode** in the app
   - **Margin Position:** Distance from page edge to first line (typically `30.0 mm`)
   - **Line Spacing:** Gap between ruled lines (standard `8.0 mm` or `9.0 mm`)

---

## 📌 Quick Reference Checklist

- [ ] Unmount pen before bed leveling
- [ ] Run bed mesh/ABL probe with pen OFF
- [ ] Mount pen again after leveling complete
- [ ] Calibrate pen touch Z height
- [ ] Measure X/Y toolhead offsets
- [ ] Input values into GCodePlotter app
- [ ] Generate test G-code and preview
- [ ] Test on scrap paper first

---

For full details, see the README and previous release notes.
