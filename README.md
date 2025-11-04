# Ham Radio Profile Page Designer 📻

**Create stunning, personalized QRZ-style profile pages with AI assistance**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform: 8KB CSS](https://img.shields.io/badge/Platform-8KB%20CSS-blue.svg)]()
[![AI: Claude Code](https://img.shields.io/badge/Best%20with-Claude%20Code-blueviolet.svg)](https://claude.ai/code)

---

## 🎯 **What is This?**

This project provides an **AI agent prompt** specifically designed to help ham radio operators create beautiful, technically-compliant profile pages for platforms like QRZ.com and similar sites with strict CSS constraints.

**Perfect for:**
- 📡 Ham radio amateurs wanting a professional online presence
- 🎨 Operators who have a design vision but don't know CSS
- ⚡ Anyone needing to work within 8KB CSS limits
- 🌍 International operators (supports CEPT/HAREC license systems)

---

## ✨ **Features**

### 🤖 **Intelligent Design Assistant**
- Upload hand-drawn sketches and get them coded
- Describe your vision in plain text
- Or follow guided questions to build your design

### 🌍 **Country-Aware**
- Automatic flag color detection from callsign prefix
- 20+ country presets (USA, UK, Germany, Romania, Japan, etc.)
- Supports international license systems (HAREC, CEPT, NOVICE)

### 🎨 **Professional Templates**
- **Standard Profile**: Full-featured layout with all sections
- **Minimalist**: Clean, simple design
- **Custom**: Your sketch becomes reality

### 📐 **Technical Compliance**
- Guaranteed under 8KB CSS limit
- No JavaScript (fully static)
- Platform-tested constraints documented
- Responsive design included

### 🎭 **Visual Elements Library**
- Animated signal strength bars
- Frequency displays
- Band activity visualizations
- Mode badges (SSB, CW, FT8, DMR, etc.)
- Country flag accents

---

## 🚀 **Quick Start**

### **Best Use: Claude Code** (Recommended)

1. **Install Claude Code** (if you haven't already)
   ```bash
   # Follow instructions at https://claude.ai/code
   ```

2. **Clone this repository**
   ```bash
   git clone https://github.com/graphblue/whoiam.git
   cd whoiam
   ```

3. **Load the agent prompt**
   - Open `HAM-PROFILE-AGENT.md` in Claude Code
   - The agent will automatically understand the full context

4. **Start designing!**
   ```
   You: "I want to create a profile page for my callsign YO3GPH"
   Agent: "73! Let's create your profile. Do you have a sketch or vision in mind?"
   ```

### **Alternative: Other AI Assistants**

This agent prompt works with other AI assistants (ChatGPT, Gemini, etc.), though Claude Code provides the best experience due to its superior code generation and file handling capabilities.

**To use with other AI:**
1. Copy the content of `HAM-PROFILE-AGENT.md` and `PLATFORM-LIMITS.md`
2. Paste it into your AI assistant
3. Add: "Please act as this agent and help me create a ham radio profile page"
4. Provide your callsign and preferences

---

## 📚 **Documentation**

### **Core Files**

| File | Description |
|------|-------------|
| `HAM-PROFILE-AGENT.md` | Complete agent prompt with instructions |
| `PLATFORM-LIMITS.md` | Technical constraints and limitations |


---

## 🎓 **How It Works**

### **Step 1: Vision Capture**
The agent asks how you want to work:
- **Upload a sketch** 📐 - Hand-drawn design? No problem!
- **Describe your vision** 💭 - "I want my callsign huge with Romanian colors..."
- **Guided questions** ❓ - Not sure? We'll ask the right questions

### **Step 2: Information Gathering**
```
- Callsign: Your amateur radio callsign
- Name: Your name
- Location: QTH, Grid Locator (e.g., KN32AL)
- Equipment: Radios, antennas, amplifiers
- Preferences: Favorite bands, modes, activities
- License Class: Including HAREC/CEPT for international operators
```

### **Step 3: Design & Generation**
The agent:
1. Detects your country from callsign prefix
2. Suggests flag colors automatically
3. Creates custom layout based on your vision
4. Generates optimized HTML + CSS
5. Ensures everything is under 8KB limit

### **Step 4: Delivery**
You receive:
- `callsign-profile.html` - Your complete page
- `callsign.css` - Minified CSS (ready to upload)
- `callsign-readable.css` - Human-readable version for editing
- `README.md` - Upload instructions

---

## 🌍 **Supported Countries**

Auto-detected flag colors for:

| Region | Countries |
|--------|-----------|
| **North America** | USA (W/K), Canada (VE), Mexico (XE) |
| **Europe** | UK (G), Germany (DL), France (F), Italy (I), Spain (EA), Romania (YO), Netherlands (PA), Belgium (ON), Slovakia (OM) |
| **Asia** | Japan (JA), South Korea (HL), Australia (VK), New Zealand (ZL) |
| **South America** | Brazil (PY), Argentina (LU) |
| **Africa** | South Africa (ZS) |

*More countries supported - see `HAM-PROFILE-AGENT.md` for full list*

---

## 📋 **Romanian License System**

Special support for Romanian ham operators:

```
Clasa I   → HAREC international equivalent
Clasa II  → HAREC international equivalent
Clasa III → Novice international equivalent
Clasa IV  → Entry-Class international equivalent
```

Note: Classes I & II qualify for full HAREC recognition for CEPT international operation.

---

## 🔧 **Technical Details**

### **Platform Constraints**
```yaml
CSS Maximum: 8,192 bytes (8KB)
JavaScript: Not allowed
External Resources: Not allowed

Blocked CSS:
  - Pseudo-elements with content: ''
  - Quoted font names ('Courier New')
  - @import statements
  - pointer-events property

Allowed CSS:
  - Full Flexbox support
  - Full CSS Grid support
  - Animations (@keyframes)
  - Transitions & Transforms
  - Media Queries
  - RGBA colors
  - Box/Text shadows
```

### **CSS Optimization**
The agent automatically:
- Minifies CSS to single-line
- Uses 3-char hex codes (#0f8 vs #00ff88)
- Removes unnecessary whitespace
- Applies decimal notation (.5 vs 0.5)
- Combines selectors
- Keeps safety margin under 8KB limit

---

## 🎨 **What You'll Get**

The agent generates a complete profile page with:

- ✅ **Prominent callsign display** with your country's flag colors
- ✅ **Animated signal bars** for authentic amateur radio feel
- ✅ **Equipment showcase** with expandable sections
- ✅ **Band activity visualization** showing your operating preferences
- ✅ **Mode badges** (SSB, CW, FT8, DMR, FM, APRS, etc.)
- ✅ **Responsive design** (works on mobile, tablet, desktop)
- ✅ **Hover effects** and smooth animations
- ✅ **Contact links** section (QRZ, HamQTH, eQSL, PSKReporter)
- ✅ **Under 8KB CSS** - guaranteed platform compliance

---

## 🤝 **Contributing**

Contributions are welcome! Here's how you can help:

### **Add Your Country**
If your country isn't in the auto-detection list:
1. Find your flag's official RGB colors
2. Add to `COUNTRY_COLORS` dictionary in `HAM-PROFILE-AGENT.md`
3. Submit a pull request

### **Share Your Profile**
Created an amazing profile? Share it!
- Open an issue with tag `show-and-tell`
- Include a screenshot or link
- Help inspire other operators!

### **Report Issues**
Found a bug or limitation?
- Open an issue with details
- Include platform error messages
- Share what didn't work

---

## ❓ **FAQ**

### **Q: Can I use this for other platforms?**
A: Yes! While optimized for 8KB CSS platforms, the generated code works anywhere that accepts HTML/CSS.

### **Q: Do I need to know CSS?**
A: No! That's the point. Just describe what you want or upload a sketch.

### **Q: Can I edit the generated CSS?**
A: Absolutely! You receive both minified and readable versions. Edit the readable version, then minify it when done.

### **Q: What if my design exceeds 8KB?**
A: The agent will automatically optimize and suggest what to remove if needed. It prioritizes visual impact.

### **Q: Does this work without Claude Code?**
A: Yes, but Claude Code provides the best experience due to superior code generation and file handling. Other AI assistants work but may require more manual steps.

### **Q: Can I commercial use this?**
A: Yes! MIT License means you can use it freely for personal or commercial purposes.

### **Q: What about JavaScript widgets (QRZ stats, ClubLog)?**
A: Platform blocks JavaScript, but you can embed iframe widgets from services that support them. See `PLATFORM-LIMITS.md` for details.

---

## 📝 **License**

MIT License - see [LICENSE](LICENSE) file for details.

**TL;DR:** Use it freely, modify it, share it. Just keep the license notice.

---

## 🔗 **Links**

- **GitHub Repository**: https://github.com/graphblue/whoiam
- **Claude Code**: https://claude.ai/code
- **QRZ.com**: https://www.qrz.com
- **Issues & Support**: https://github.com/graphblue/whoiam/issues

---

## 🙏 **Credits**

**Project Creator**: [GraphBlue](https://github.com/graphblue)
**Optimized for**: [Claude Code](https://claude.ai/code) by Anthropic
**License**: Creative Commons Attribution 4.0 International

**Special Thanks:**
- The global amateur radio community
- Anthropic for Claude's advanced AI capabilities
- All ham operators who will use and improve this tool

---

## 📡 **73!**

*May your signals be strong and your QSOs plentiful!*

---

**Last Updated**: 2025-11-04
**Version**: 1.0
**Status**: Production Ready ✅
