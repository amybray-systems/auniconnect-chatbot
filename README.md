# 🤖 AuniConnect Smart Chatbot Demo

> An intelligent employment assistant that detects worker confusion, provides personalized answers, and educates contingent workers about their employment relationship.

**[🚀 Try Live Demo](https://amybray-systems.github.io/auniconnect-chatbot/)**

---

## 🎯 What This Solves

**The Problem:** Contingent workers constantly confuse who their employer is, where to get benefits, and who handles their PTO. They ask their client manager questions that should go to their EOR/staffing company.

**The Solution:** This chatbot detects employment type (W2 vs 1099), identifies client/employer companies, and provides crystal-clear answers with automatic education about the "three players" (Client, EOR, AuniConnect).

---

## ✨ Key Features

### 🧠 Smart Detection
- **Auto-detects employment type** from questions (W2 Contingent vs 1099 Contractor)
- **Extracts company names** from natural language (client and EOR)
- **Corrects common confusion** ("My manager at Google" vs "My manager at Randstad")
- **Handles typos** automatically (benifits → benefits, vaccation → vacation)

### 🎭 Dual Modes
- **👤 Employee Mode:** Answers worker questions with personalized, type-specific responses
- **👔 Manager Mode:** Helps managers coach teams and route questions correctly

### 🎯 Type-Specific Answers
- **W2 Contingent:** Benefits from EOR, PTO policies, payroll info, timesheet systems
- **1099 Contractors:** Reality checks (no benefits, no PTO), invoicing, tax implications
- **Smart Filtering:** Only shows relevant answers based on detected employment type

### 🔒 Smart Controls
- **Auto-disables EOR selection** when 1099 is selected (contractors don't have employers!)
- **Visual feedback** with badges showing detected type, client, and employer
- **Quick Setup mode** for instant demo with pre-set scenarios

### 📚 Educational
- Explains the "three players" relationship (Client, EOR, AuniConnect)
- Clarifies WHO handles WHAT (pay, benefits, work tasks)
- Proactively corrects misunderstandings

---

## 🚀 Quick Start (10 Minutes)

### 1. Create GitHub Repo
1. Go to [github.com/new](https://github.com/new)
2. Name: `auniconnect-chatbot`
3. Make it **Public**
4. Add README
5. License: MIT
6. Click "Create repository"

### 2. Download & Save Files

**File 1: `index.html`** (Main chatbot)
- Copy the full HTML code from the artifact
- Save as `index.html` (exact name!)

**File 2: `README.md`** (This file)
- Copy this entire README
- Replace `yourusername` with YOUR GitHub username
- Save as `README.md`

### 3. Upload to GitHub
1. Click "Add file" → "Upload files"
2. Drag `index.html`
3. Commit: "Add smart chatbot"
4. Click "Commit changes"

### 4. Enable GitHub Pages
1. Settings → Pages (left sidebar)
2. Source: **main** branch
3. Folder: **/ (root)**
4. Click "Save"
5. Wait 2-3 minutes ⏰

### 5. Test Your Demo
Visit: `https://yourusername.github.io/auniconnect-chatbot/`

---

## 🎬 How to Demo

### Quick Demo (2 minutes)

1. **Click "Quick Setup"**
   - Select "W2 Contingent"
   - Select "Google" (client)
   - Select "Randstad" (employer)

2. **Ask: "What are my benefits?"**
   - Watch the detection badge appear
   - See personalized answer with company names

3. **Ask: "Who is my manager at Google?"**
   - Watch the confusion clarification
   - See the "three players" explanation

4. **Switch to "1099 Contractor"**
   - Notice EOR buttons automatically disable
   - Ask about benefits
   - See reality check: "You get ZERO benefits"

### Full Demo (5 minutes)

**Part 1: Show Detection (1 min)**
```
"I work at Microsoft through Adecco"
"What are my benefits?"
```
→ Point out auto-detected badges and personalized answer

**Part 2: Show Confusion Correction (2 min)**
```
"My boss at Microsoft said to contact HR about PTO"
```
→ Watch bot detect confusion and clarify the relationship

**Part 3: Show Manager Mode (2 min)**
- Switch to Manager Mode
- Ask: "My team member wants PTO"
- Show how it helps managers route questions

---

## 📝 How to Add More Q&A Pairs

Find the `demoData` object in `index.html` (around line 450) and add new entries:

### Employee Mode Example:
```javascript
{
    keywords: ['sick leave', 'sick day', 'call in sick'],
    types: ['W2_Contingent'],  // Options: 'W2_Contingent', '1099', or 'All'
    answer: "Sick Leave for W2 Contingent:\n\n**How to Call In:**\n• Notify [EOR]\n• Also tell your supervisor at [Client Company]\n\n**Sick Days:** 5-10 per year\n**Questions:** Contact [EOR]'s HR"
},
```

### Manager Mode Example:
```javascript
{
    keywords: ['1:1', 'one on one', 'check in'],
    types: ['All'],
    answer: "Effective 1:1s:\n\n**Quick Agenda:**\n• Wins this week\n• Top 3 priorities\n• Blockers\n• What you need from me"
},
```

### Formatting Tips:
- `\n\n` = New paragraph
- `**Text**` = Bold text
- `• Item` = Bullet point
- `[EOR]` = Auto-replaced with actual employer name
- `[Client Company]` = Auto-replaced with client name

---

## 🎨 Customization

### Add Your Logo
Replace the bot avatar (around line 50):
```html
<div class="bot-avatar">A</div>
<!-- Replace with: -->
<img src="your-logo.png" style="width:50px;height:50px;border-radius:50%">
```

### Change Colors
Update the gradient (around line 15):
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
/* Replace with your brand colors */
```

### Add Contact Info
Add to welcome message (around line 720):
```javascript
"Questions? Contact sales@auniconnect.com"
```

---

## 🔗 Integration Options

### Link from Your Main Site
```html
<a href="https://amybray-systems.github.io/auniconnect-chatbot/" 
   target="_blank"
   style="background: #667eea; color: white; padding: 12px 24px; 
          border-radius: 8px; text-decoration: none; font-weight: bold;">
   🤖 Try Our Smart Chatbot Demo
</a>
```

### Embed in Your Site (iframe)
```html
<iframe 
  src="https://amybray-systems.github.io/auniconnect-chatbot/" 
  width="100%" 
  height="800px" 
  frameborder="0">
</iframe>
```

### Create Dedicated Page
Point `auniconnect.com/chatbot-demo` to your GitHub Pages URL

---

## 📱 Sharing Your Demo

### LinkedIn Post Template
```
🤖 Excited to share our new Smart Employment Chatbot!

It solves a huge problem in contingent workforce management:
✅ Auto-detects W2 vs 1099 workers
✅ Clarifies who handles benefits, PTO, payroll
✅ Educates workers about the "three players"
✅ Helps managers route questions correctly

Try it: [your-url]

#WorkforceManagement #AI #Chatbot #HR #ContingentWorkforce
```

### Email Signature
```
🤖 See Our Smart Chatbot Demo: [your-url]
```

---

## 🛠️ Technical Details

- **Pure HTML/CSS/JavaScript** - No build process needed
- **Responsive design** - Works on mobile/tablet/desktop
- **No backend required** - Runs entirely in browser
- **Fast & lightweight** - ~50KB total size
- **Keyboard accessible** - Press Enter to send messages

---

## 🆘 Troubleshooting

**Demo doesn't load?**
- Verify file is named `index.html` (not `chatbot.html`)
- Wait full 3 minutes after enabling GitHub Pages
- Clear browser cache (Ctrl+F5 or Cmd+Shift+R)

**Companies not detected?**
- Use exact capitalization: "Google" not "google"
- Or use Quick Setup buttons for guaranteed detection

**EOR buttons not disabling?**
- Make sure you selected an employment type first
- Click "W2 Contingent" first, then EOR should enable
- Click "1099 Contractor" and EOR should disable

**Want to reset?**
- Refresh the page to start fresh
- Or switch modes (Employee ↔ Manager)

---

## 📊 Demo Scenarios

### Scenario 1: Confused W2 Worker
```
Setup: W2 Contingent + Google + Randstad
Ask: "My manager at Google won't answer my benefits question"
Result: Bot clarifies that Google is client, Randstad handles benefits
```

### Scenario 2: 1099 Reality Check
```
Setup: 1099 Contractor + Microsoft
Ask: "When do I get PTO?"
Result: Bot explains no PTO exists for contractors
```

### Scenario 3: Manager Coaching
```
Mode: Manager
Ask: "How do I handle my team's PTO questions?"
Result: Clear instructions on routing W2/1099 questions
```

---

## 🎯 Key Differentiators

What makes this chatbot special:

1. **Context-aware**: Remembers employment type, client, employer across conversation
2. **Educational**: Doesn't just answer - it teaches the relationship
3. **Proactive**: Detects and corrects confusion before workers get frustrated
4. **Dual-purpose**: Serves both employees AND managers
5. **Smart filtering**: Only shows relevant answers (no 1099 workers seeing W2 benefits info!)

---

## 📈 Future Enhancements

Potential additions:
- [ ] Multi-language support (Spanish, Mandarin)
- [ ] Voice input
- [ ] Live data integration (real PTO balances, paycheck dates)
- [ ] Export conversation transcripts
- [ ] Analytics dashboard (common questions, confusion points)
- [ ] Mobile app version

---

## 📄 License

MIT License - Feel free to use and modify for your business.

---

## 🤝 Contact

Questions about implementation or customization?

**Built by:** Amy Bray Systems  
**Email:** amybray0315@gmail.com  

---

## 🌟 Show Your Support

If this helps your business:
- ⭐ Star this repo
- 🔗 Share on LinkedIn
- 📧 Send feedback
- 💼 Let's discuss custom implementations!

---

**Last Updated:** January 2025  
**Version:** 2.0 (with smart employment type filtering and EOR controls)
