# MMM Unwrapped Website

A professional multi-page website for MMM Unwrapped - Transparent Media Mix Modeling solution.

## 📁 File Structure

```
├── index.html          # Homepage
├── features.html       # Product features page
├── team.html          # Team/About page
├── case-studies.html  # Case studies page
├── contact.html       # Contact form page
├── styles.css         # Shared stylesheet (ALL design is here)
├── script.js          # Shared JavaScript
└── README.md          # This file
```

## 🚀 How to Use

1. **Open the website**: Double-click `index.html` to open in your browser
2. **Navigate**: Click the menu items to visit different pages
3. **All files must be in the same folder** for links to work properly

## 🎨 HOW TO CHANGE THE DESIGN

**IMPORTANT: All design changes happen in `styles.css` - NOT in the HTML files!**

### Changing Colors

Open `styles.css` and look for the `:root` section at the top:

```css
:root {
    --primary-blue: #1e3a8a;    /* Main blue color - change this! */
    --accent-teal: #14b8a6;     /* Teal accent color - change this! */
    --light-bg: #f8fafc;        /* Light background color */
    --dark-text: #1e293b;       /* Text color */
    --gray-text: #64748b;       /* Secondary text color */
}
```

**Example:** To change from blue to purple theme:
```css
:root {
    --primary-blue: #7c3aed;    /* Purple instead of blue */
    --accent-teal: #f59e0b;     /* Orange instead of teal */
}
```

### Common Design Changes

**1. Change font:**
Find this line in `styles.css` (around line 15):
```css
font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto...
```
Replace with:
```css
font-family: 'Georgia', serif;  /* Or any font you prefer */
```

**2. Make sections more/less spacious:**
Find this line in `styles.css` (around line 400):
```css
section {
    padding: 5rem 2rem;  /* Change 5rem to make bigger/smaller */
}
```

**3. Change button style:**
Find `.cta-button` in `styles.css` (around line 140) and modify:
```css
.cta-button {
    background: var(--accent-teal);
    border-radius: 8px;    /* Make it 25px for rounded buttons */
    padding: 1rem 2rem;    /* Change size */
}
```

**4. Adjust hero section:**
Find `.hero` in `styles.css` (around line 90) and modify the gradient:
```css
background: linear-gradient(135deg, #your-color-1 0%, #your-color-2 100%);
```

**5. Change card shadows:**
Find `.feature-card` in `styles.css` (around line 450):
```css
box-shadow: 0 4px 6px rgba(0,0,0,0.1);  /* Adjust numbers for depth */
```

## 📝 Adding Content

### Adding Team Members

Open `team.html` and replace the placeholder section with actual team member cards.
See the commented HTML in the file for the structure.

### Adding Case Studies

Open `case-studies.html` and add case study cards.
See the commented HTML in the file for the structure.

## 🔧 Making the Contact Form Work

The form currently shows an alert. To make it actually send emails:

**Option 1: Use a service like Formspree**
1. Go to formspree.io
2. Get your form endpoint
3. In `contact.html`, change the form tag to:
```html
<form action="https://formspree.io/f/YOUR_ID" method="POST">
```

**Option 2: Use Netlify Forms (if hosting on Netlify)**
Add `netlify` attribute to the form tag:
```html
<form netlify>
```

**Option 3: Connect to your own backend**
Modify the JavaScript in `script.js` to send to your API.

## 🌐 Next Steps: Using with Claude Code

Once you're happy with the design, you can use Claude Code to:
1. Add a backend for the contact form
2. Connect to a database for case studies
3. Add authentication for admin panel
4. Implement analytics tracking
5. Add interactive data visualizations
6. Set up hosting and deployment

**Prompt for Claude Code:**
```
I have a multi-page website for MMM Unwrapped. The files are in [location]. 
I need you to:
1. Set up proper form handling for the contact form
2. Create a simple CMS for managing case studies and team members
3. Deploy it to [Netlify/Vercel/your preference]

The current files are: index.html, features.html, team.html, case-studies.html, 
contact.html, styles.css, and script.js
```

## 💡 Design Tips

1. **Keep it simple**: Don't change too many things at once
2. **Test on mobile**: Open in browser and use developer tools (F12) to test responsive design
3. **Consistency**: Use the color variables instead of hardcoding colors
4. **Backup first**: Before making changes, save a copy of `styles.css`

## 🎨 Quick Design Templates

Want a completely different look? Here are some quick color scheme changes:

**Professional Corporate:**
```css
--primary-blue: #1e40af;
--accent-teal: #3b82f6;
```

**Modern Tech:**
```css
--primary-blue: #6366f1;
--accent-teal: #ec4899;
```

**Elegant Minimal:**
```css
--primary-blue: #0f172a;
--accent-teal: #64748b;
```

**Bold Startup:**
```css
--primary-blue: #7c3aed;
--accent-teal: #f59e0b;
```

## 📞 Questions?

If something doesn't work or you need help with customization, you can:
1. Ask Claude (me!) for specific changes
2. Use Claude Code for more complex modifications
3. Check browser console (F12) for errors

---

**Pro Tip:** The easiest way to experiment with design is to:
1. Open `styles.css` in a text editor
2. Open `index.html` in your browser
3. Make a change in `styles.css` and save
4. Refresh the browser to see the change
5. Repeat until you like it!
