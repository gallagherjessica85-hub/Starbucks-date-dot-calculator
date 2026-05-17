# ☕ Starbucks Date Dot Calculator

A beautifully designed, accessible web tool for quickly determining when to discard food and beverages based on Starbucks' date dot expiration system.

## 🎯 Features

- **Real-time Clock Display** - Shows current time, date, and day
- **Color-Coded Expiration Timeline** - Each day of the week has a unique color for quick identification
- **One-Click Copy** - Easily copy expiration details to clipboard for reference
- **Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices
- **Timezone Aware** - Automatically detects and displays your local timezone
- **Print-Friendly** - Generate a printable expiration guide
- **Accessible** - Full ARIA labels, keyboard navigation, and screen reader support
- **No Dependencies** - Vanilla JavaScript, no frameworks or external libraries needed

## 📋 Expiration Groups

| Label | Duration | Examples |
|-------|----------|----------|
| **24H** | 24 hours | Whip Cream, Chai, Mocha |
| **48H** | 48 hours | Sweet Cream, Lemonade, Frap Roast |
| **3D** | 3 days | Pastries, Refresher Bases |
| **5D** | 5 days | Refresher Inclusions |
| **6D** | 6 days | Cold Brew (dropped) |
| **7D** | 7 days | Cold Bar Powders, Egg Bites, Whole Bean Coffee |
| **2WK** | 2 weeks | Caramel Sauce, White Mocha, Pistachio Sauce |

## 🚀 Getting Started

1. **Open `index.html`** in any modern web browser
2. View real-time expiration timelines for all date dot categories
3. Use the **copy button** on any card to copy expiration details
4. Check your **timezone** at the top to ensure accuracy

## 🎨 Design Highlights

- **Starbucks-Inspired Color Palette** - Dark green (#00704A) and gold (#CBA258) branding
- **Premium Typography** - Bebas Neue, Inter, and DM Mono fonts
- **Smooth Animations** - Subtle transitions and a pulsing indicator
- **Ambient Effects** - Blurred gradient blobs for visual depth
- **Day-Specific Colors** - Sunday through Saturday each have unique accent colors

## ♿ Accessibility

✅ **WCAG 2.1 Compliant Features:**
- Semantic HTML with proper heading hierarchy
- Full ARIA labels on interactive elements
- Skip-to-content link for keyboard navigation
- Screen reader optimized with `aria-live` regions
- Color is not the only indicator of information
- Adequate color contrast ratios
- Keyboard navigation support
- Focus states on interactive elements

## 🔧 Technical Details

### Browser Support
- ✅ Chrome, Firefox, Safari, Edge (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)
- ⚠️ IE11 (with clipboard fallback)

### Performance
- **Light weight** - Single HTML file, ~15KB
- **No external API calls** - Runs entirely in the browser
- **Efficient rendering** - Smart update intervals (every second for display, every minute for data)
- **Tab focus detection** - Automatically re-syncs when tab regains focus

### JavaScript Features
- **Event listeners** instead of inline handlers
- **Async/await** for clipboard operations
- **Fallback support** for older browsers (IE11 clipboard API)
- **Timezone detection** using `Intl.DateTimeFormat()`
- **Visibility API** for tab focus detection

## 📱 Responsive Breakpoints

- **Desktop** - Full layout with 3-column card grid
- **Tablet** - Optimized spacing and readable typography
- **Mobile** (<420px) - Single-column layout with adjusted font sizes

## 🖨️ Print Support

Click **Print** (Cmd+P / Ctrl+P) to generate a printer-friendly version:
- Removes decorative elements (blobs, footer)
- Hides interactive buttons
- Prevents page breaks within cards
- Clean black-on-white styling

## 🎯 How It Works

1. **Gets current time** from your device
2. **Calculates expiration dates** by adding duration minutes to current time
3. **Determines day of week** for each expiration date
4. **Applies color coding** based on the day
5. **Updates every minute** to keep data fresh
6. **Re-syncs on tab focus** to prevent drift

## 📝 Customization

To modify items or expiration times, edit the `GROUPS` array in the JavaScript:

```javascript
const GROUPS = [
  { label: '24H', duration: '24 hours', mins: 1*24*60, items: ['Item 1', 'Item 2'] },
  // Add or modify groups here
];
```

## 🎓 Learning Resources

This project demonstrates:
- Vanilla JavaScript (no frameworks)
- CSS Grid and Flexbox
- Accessibility best practices (WCAG)
- Responsive web design
- Browser APIs (Clipboard, Visibility, Intl)
- Event handling and DOM manipulation
- Print media queries

## 📄 License

This project is open source and available for personal and commercial use.

## 🤝 Contributing

Found a bug or have a suggestion? Feel free to [open an issue](https://github.com/gallagherjessica85-hub/Starbucks-date-dot-calculator/issues) or submit a pull request.

---

**Last Updated:** 2026-05-17  
**Version:** 2.0 (Improved & Accessible)
