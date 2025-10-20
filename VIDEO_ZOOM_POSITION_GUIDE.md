# 🎬 Video Customization Guide - Independent Zoom & Position Control

This guide explains how to independently control the **zoom level** and **position (X, Y shift)** for each project video in your portfolio.

---

## 📋 Quick Reference

Each video now has three customizable attributes:

| Attribute | What it Does | Example Values |
|-----------|--------------|----------------|
| `data-zoom` | Controls video zoom/scale | `1.0` (normal), `1.2` (20% bigger), `1.5` (50% bigger) |
| `data-shift-x` | Shifts video left/right in pixels | `0` (centered), `20` (right), `-20` (left) |
| `data-shift-y` | Shifts video up/down in pixels | `0` (centered), `-10` (up), `10` (down) |

---

## 🎯 Current Video Settings

Here are the current settings for each project video:

### 1. **Surgical-Grade Brain Tissue Extraction using ML**
```html
data-zoom="1.2" 
data-shift-x="15" 
data-shift-y="-10"
```
- **Zoom**: 120% (slightly enlarged)
- **Position**: Shifted 15px right, 10px up

---

### 2. **AI-Powered Video Dubbing with Lip-Sync**
```html
data-zoom="1.4" 
data-shift-x="30" 
data-shift-y="-10"
```
- **Zoom**: 140% (moderately enlarged)
- **Position**: Shifted 30px right, 10px up

---

### 3. **Lesion Master - AI-Powered Medical Image Segmentation**
```html
data-zoom="1.0" 
data-shift-x="0" 
data-shift-y="0"
```
- **Zoom**: 100% (normal size)
- **Position**: Centered (no shift)

---

### 4. **Brain Tumor Visualisation in 3D**
```html
data-zoom="1.5" 
data-shift-x="30" 
data-shift-y="-10"
```
- **Zoom**: 150% (significantly enlarged)
- **Position**: Shifted 30px right, 10px up

---

### 5. **Advanced Time-Series Forecasting for Market Volatility**
```html
data-zoom="1.0" 
data-shift-x="0" 
data-shift-y="0"
```
- **Zoom**: 100% (normal size)
- **Position**: Centered (no shift)

---

### 6. **Quantitative Analysis of Market Sentiment using NLP**
```html
data-zoom="1.0" 
data-shift-x="0" 
data-shift-y="0"
```
- **Zoom**: 100% (normal size)
- **Position**: Centered (no shift)

---

### 7. **Financial Modeling: Black-Scholes Implementation**
```html
data-zoom="1.0" 
data-shift-x="0" 
data-shift-y="0"
```
- **Zoom**: 100% (normal size)
- **Position**: Centered (no shift)

---

### 8. **Real-Time IoT Air Quality Monitor**
```html
data-zoom="1.4" 
data-shift-x="10" 
data-shift-y="-10"
```
- **Zoom**: 140% (moderately enlarged)
- **Position**: Shifted 10px right, 10px up

---

### 9. **Object Sensing and Identification using IoT**
```html
data-zoom="1.0" 
data-shift-x="0" 
data-shift-y="0"
```
- **Zoom**: 100% (normal size)
- **Position**: Centered (no shift)

---

## 🛠️ How to Customize

### Step 1: Find the Video in `index.html`

Each video looks like this:
```html
<video class="project-video" autoplay muted loop playsinline 
       data-zoom="1.0" 
       data-shift-x="0" 
       data-shift-y="0">
    <source src="Splash/[video-name].mp4" type="video/mp4">
</video>
```

### Step 2: Adjust the Values

#### **To Zoom In/Out:**
- Change `data-zoom` value:
  - `1.0` = Normal size (100%)
  - `1.2` = 20% bigger
  - `1.5` = 50% bigger
  - `0.8` = 20% smaller
  - `2.0` = Double size (200%)

#### **To Shift Left/Right:**
- Change `data-shift-x` value:
  - `0` = Centered horizontally
  - Positive numbers (e.g., `20`) = Shift RIGHT
  - Negative numbers (e.g., `-20`) = Shift LEFT

#### **To Shift Up/Down:**
- Change `data-shift-y` value:
  - `0` = Centered vertically
  - Positive numbers (e.g., `10`) = Shift DOWN
  - Negative numbers (e.g., `-10`) = Shift UP

---

## 📝 Example: Customizing a Specific Video

Let's say you want to make the **Lesion Master** video:
- **Zoom**: 130% (1.3x bigger)
- **Position**: Shift 20px right and 5px up

**Before:**
```html
<video class="project-video" autoplay muted loop playsinline 
       data-zoom="1.0" 
       data-shift-x="0" 
       data-shift-y="0">
    <source src="Splash/lesion master.mp4" type="video/mp4">
</video>
```

**After:**
```html
<video class="project-video" autoplay muted loop playsinline 
       data-zoom="1.3" 
       data-shift-x="20" 
       data-shift-y="-5">
    <source src="Splash/lesion master.mp4" type="video/mp4">
</video>
```

---

## 🎨 Tips for Perfect Centering

1. **Start with default values** (`data-zoom="1.0"`, both shifts at `"0"`)
2. **Adjust zoom first** to get the desired size
3. **Then fine-tune position** using shift values
4. **Test in browser** after each change (refresh the page)
5. **Use small increments** (5-10 pixels at a time) for precise positioning

---

## 🔍 Common Adjustments

### Video appears too small?
- Increase `data-zoom` to `1.2`, `1.3`, or `1.4`

### Video is off-center horizontally?
- Adjust `data-shift-x`:
  - If video is too far left: increase value (e.g., from `0` to `20`)
  - If video is too far right: decrease value (e.g., from `20` to `0` or `-10`)

### Video is off-center vertically?
- Adjust `data-shift-y`:
  - If video is too low: decrease value (e.g., from `0` to `-10`)
  - If video is too high: increase value (e.g., from `-10` to `0` or `5`)

### Video looks cropped?
- The video container height is set to 250px. If zooming causes excessive cropping:
  1. Find line ~267 in `index.html`:
     ```css
     .project-animation-container {
         height: 250px;  /* Increase this value */
     ```
  2. Change to `350px` or `400px` for more space

---

## 🖥️ Testing Your Changes

1. **Save** `index.html` after making changes
2. **Refresh** your browser (or use Ctrl+F5 / Cmd+Shift+R for hard refresh)
3. **Scroll to the Projects section** to see your changes
4. **Repeat** until satisfied with the positioning

---

## ⚡ Quick Copy-Paste Templates

### Centered, Normal Size
```html
data-zoom="1.0" 
data-shift-x="0" 
data-shift-y="0"
```

### Slightly Zoomed, Centered
```html
data-zoom="1.2" 
data-shift-x="0" 
data-shift-y="0"
```

### Moderately Zoomed, Shifted Right & Up
```html
data-zoom="1.4" 
data-shift-x="20" 
data-shift-y="-10"
```

### Heavily Zoomed, Shifted Right & Up
```html
data-zoom="1.6" 
data-shift-x="30" 
data-shift-y="-15"
```

---

## 🚀 Advanced: Global Container Settings

If you want to change settings for ALL videos at once:

### Background Color
Find line ~267 in `index.html`:
```css
.project-animation-container {
    background: #000;  /* Black background */
}
```
Change `#000` to any color (e.g., `#111` for dark gray)

### Container Height
Find line ~267:
```css
.project-animation-container {
    height: 250px;  /* Change to 300px, 350px, etc. */
}
```

### Video Fit Mode
Find line ~277:
```css
.project-video {
    object-fit: contain;  /* Change to 'cover' to fill space */
}
```
- `contain` = Shows full video (may add black bars)
- `cover` = Fills space completely (may crop edges)

---

## 📞 Need Help?

If you're having trouble:
1. Check that you saved the file
2. Do a hard refresh in your browser
3. Make sure values are in quotes (e.g., `data-zoom="1.2"` not `data-zoom=1.2`)
4. Verify there are no typos in attribute names

---

## 🎉 You're All Set!

Each video now has independent control over its zoom and position. Experiment with different values to find the perfect display for each project! 

**Happy customizing!** 🚀
