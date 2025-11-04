# Platform Constraints Documentation
## Ham Radio Profile Site - CSS/HTML Limits

### **Discovered Through Testing (2025-11-03)**

---

## ✅ **What Works**

### **CSS (Maximum 8,192 bytes)**
- ✅ All basic CSS properties (colors, borders, padding, margins)
- ✅ Flexbox & CSS Grid layouts
- ✅ Animations (`@keyframes`)
- ✅ Transitions
- ✅ Transforms (translate, scale, rotate)
- ✅ Text shadows
- ✅ Box shadows
- ✅ Gradients (linear, radial)
- ✅ RGBA colors
- ✅ Shorthand hex colors (`#0f8` instead of `#00ff88`)
- ✅ Pseudo-classes (`:hover`, `:nth-child()`)
- ✅ Media queries (responsive design)
- ✅ Border radius
- ✅ Opacity

### **HTML**
- ✅ All semantic HTML5 tags
- ✅ `<details>` and `<summary>` (native collapse, no JS needed)
- ✅ Inline SVG
- ✅ Data URI images (`data:image/svg+xml,...`)
- ✅ External stylesheets (`<link rel="stylesheet">`)
- ✅ Tables
- ✅ Forms (checkboxes, inputs)
- ✅ Iframes (for embedding widgets)

---

## ❌ **What Doesn't Work**

### **Blocked CSS Features**
- ❌ Pseudo-elements with `content: ''` property (`:before`, `:after` with content)
- ❌ `@import` statements
- ❌ `pointer-events` property
- ❌ External font imports via `@import`
- ❌ Some complex gradients with multiple lines in source
- ❌ **Single quotes in font-family** (e.g., `font-family:'Courier New',monospace`) - CRITICAL BUG
- ❌ **Double quotes in font-family** (assumed, use generic fonts only)

### **JavaScript**
- ❌ **NO JavaScript at all** (completely blocked)
- ❌ No `<script>` tags
- ❌ No inline JS (`onclick`, etc.)
- ❌ No external JS files

### **File Size Limits**
- ❌ **CSS: Maximum 8,192 bytes (8KB)** - strictly enforced
- ❌ Platform counts actual byte size (not characters)
- ❌ Newlines count toward limit

---

## 💡 **Optimization Strategies**

### **CSS Minification Techniques**
1. **Remove all whitespace and newlines** - Save ~100-200 bytes
2. **Use short hex colors**: `#0f8` instead of `#00ff88` - Save 3 bytes per color
3. **Use decimal notation**: `.3` instead of `0.3` - Save 1 byte per value
4. **Combine selectors** where possible
5. **Remove comments** (obviously)
6. **Use shorthand properties**: `margin: 0` instead of `margin-top: 0; margin-bottom: 0`
7. **Avoid repetition**: Use combined classes
8. **Use generic font families**: `monospace` instead of `'Courier New',monospace` - Saves bytes AND avoids parser bugs

### **Example Optimizations**
```css
/* Before (verbose) */
background-color: #00ff88;
rgba(0, 255, 136, 0.3)

/* After (optimized) */
background: #0f8;
rgba(0,255,136,.3)
```

---

## 🎯 **Widget Integration (No-JS Workarounds)**

### **Embeddable Widgets That Work**
Since JavaScript is blocked, use **iframe embeds**:

1. **QRZ.com Badge**
   ```html
   <iframe src="https://www.qrz.com/db/CALLSIGN" width="300" height="150"></iframe>
   ```

2. **PSKReporter Map**
   ```html
   <iframe src="https://pskreporter.info/pskmap.html?preset&callsign=CALLSIGN"
           width="100%" height="400"></iframe>
   ```

3. **DXCluster Spots** (via external embed services)
   - Use static image badges or RSS-to-HTML services
   - Some ham sites offer non-JS spot widgets

4. **HamQTH Profile**
   ```html
   <iframe src="https://www.hamqth.com/CALLSIGN" width="300" height="150"></iframe>
   ```

5. **Band Conditions** (static images)
   ```html
   <img src="https://www.hamqsl.com/solar.html" alt="Solar conditions">
   ```

### **Static Alternatives**
- Use **static images** that auto-refresh (some services provide this)
- Link to external pages instead of embedding
- Display static data with manual updates

---

## 📐 **Best Practices for 8KB Limit**

### **Priority List** (what to include in limited space)
1. ✅ Core layout (grid, flexbox)
2. ✅ Hero section styling (call sign)
3. ✅ Card/section styling
4. ✅ Basic colors and shadows
5. ✅ Hover effects (best bang for buck)
6. ✅ One or two keyframe animations
7. ✅ Responsive breakpoints (mobile, tablet, desktop)
8. ⚠️ Advanced animations (if space allows)
9. ⚠️ Multiple color themes (too expensive)

### **What to Cut if Over Limit**
- Extra animations
- Redundant hover effects
- Very detailed responsive tweaks
- Non-essential shadows
- Excessive border-radius variations

---

## 🔧 **Testing Checklist**

Before uploading, verify:
- [ ] CSS file is **under 8,192 bytes**
- [ ] No `content: ''` properties used
- [ ] No JavaScript anywhere
- [ ] No `@import` statements
- [ ] Test on actual platform (not just local)
- [ ] Check mobile responsiveness
- [ ] Verify all animations work
- [ ] Ensure iframes load correctly

---

## 📊 **File Size Reference**

```
8,192 bytes = Maximum CSS allowed
8,056 bytes = Working example (ham-profile-compact.css)
  136 bytes = Safety margin
```

**Tip**: Aim for **7,900-8,000 bytes** to leave safety margin for platform variations.

---

## 🎨 **Design Philosophy for Constraints**

Given the 8KB CSS limit:
- **Prioritize visual impact** over quantity of effects
- **Use animations strategically** (2-3 well-placed animations > 10 mediocre ones)
- **Leverage CSS Grid** efficiently (powerful layouts, minimal code)
- **Combine similar styles** into reusable classes
- **Focus on hover effects** (high impact, low cost)
- **Use color psychology** (neon glows, shadows, gradients)

---

## 🌐 **Ham Radio Specific Considerations**

### **Authentic Data Sources**
- QRZ.com - Primary callsign database
- HamQTH.com - European alternative
- PSKReporter - Digital mode activity
- DXCluster - Real-time DX spots
- LOTW (Logbook of the World) - Confirmations
- eQSL - Electronic QSL cards

### **Important Profile Elements**
- Call sign (large, prominent)
- Grid locator (e.g., KN32AL)
- License class
- Station equipment
- Favorite bands/modes
- Awards and achievements
- QSL card gallery
- Recent contacts log

---

## 📚 **Additional Resources**

- CSS Minification: Use online tools or write single-line CSS
- Color optimization: https://www.colorhexa.com/ (find shortest hex codes)
- Grid locator: https://www.levinecentral.com/ham/grid_square.php
- Band planning: http://www.arrl.org/band-plan

---

**Last Updated**: 2025-11-03
**Platform**: Ham Radio Profile Site (Unnamed)
**Tested By**: BMad Orchestrator AI
