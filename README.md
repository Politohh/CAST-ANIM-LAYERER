<h1 align="center">
  <br>
  CAST ANIM LAYERER
  <br>
</h1>

<h4 align="center">Layer .cast animations together by overriding bones from an overlay onto a base animation.</h4>

<div align="center">
  <a href="https://github.com/Politohh/CAST-ANIM-LAYERER/releases"><img src="https://img.shields.io/github/downloads/Politohh/CAST-ANIM-LAYERER/total"></a>
  <a href="https://paypal.me/politoggs"><img src="https://img.shields.io/badge/Donate-Paypal-orange?style=flat-square"></a>
</div>

<p align="center">
  <a href="#how-it-works">How it works</a> •
  <a href="#preview">Preview</a> •
  <a href="#requirements">Requirements</a> •
  <a href="#installation">Installation</a> •
  <a href="#usage">Usage</a> •
  <a href="#credits">Credits</a>
</p>

---

## How it works

CAST ANIM LAYERER takes two `.cast` animation files and combines them into one.

- The **base animation** provides the full-body motion (e.g. a walk cycle)
- The **overlay animation** overrides specific bones on top of it (e.g. a torso/upper-body animation)

Every bone present in the overlay replaces the matching bone from the base. All other bones from the base are kept untouched. The output is automatically named using the internal animation name fields from both files:

```
overlay_anim_ON_base_anim.cast
```

---

## Preview

**Base animation** — full body walk cycle

![base](pb_combatrun_right_loop.gif)

**Overlay animation** — upper body first raise

![overlay](pt_rifle_stand_firstraise.gif)

**Result** — overlay layered on top of base

![result](pt_rifle_stand_firstraise_ON_pb_combatrun_right_loop.gif)

---

## Requirements

- **Python 3.x** — [Download](https://www.python.org/downloads/)
- **cast.py** — official Cast library by [@dtzxporter](https://github.com/dtzxporter/cast)

---

## Installation

1. Download the [latest release](https://github.com/Politohh/CAST-ANIM-LAYERER/releases)
2. Place these files all in the same folder:
   - `cast_anim_merger.py`
   - `merge_anims.bat`
   - `cast.py` (from [here](https://github.com/dtzxporter/cast/blob/master/libraries/python/cast.py))

---

## Usage

### Drag & Drop
Select your **base** `.cast` file and your **overlay** `.cast` file, then drag both onto `merge_anims.bat` in that order.

> ⚠️ Order matters — drag the **base first**, overlay second.

### Command Line
```
python cast_anim_merger.py base.cast overlay.cast
```
Optional custom output path:
```
python cast_anim_merger.py base.cast overlay.cast custom_output.cast
```

### Output
The merged `.cast` file is saved in the same folder as your base animation, automatically named after the internal animation names:
```
overlay_anim_ON_base_anim.cast
```

---

## Credits

- **[dtzxporter](https://github.com/dtzxporter)** — Cast format & cast.py library
- **[Scobalula](https://github.com/Scobalula)** — Original SEModel ModelMerger concept

---

**Please contact me if you find any bugs or have any suggestions.**
#### Twitter: @thatkidpolito
#### Discord: polito#2491
