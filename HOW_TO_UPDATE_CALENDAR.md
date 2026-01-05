# 📅 How to Update the Calendar (5 Minutes Monthly)

## Where to Update

File: `_includes/events.html`

Look for the "Upcoming Events" section (around line 14-53)

---

## What to Update

The "Coming Up Next" section shows the next 3 upcoming events. Update this at the **beginning of each month**.

---

## Monthly Update Process

### **Step 1: Remove Past Events**
Delete any events that have already happened.

### **Step 2: Add New Events**
Add the next event to keep showing 3 upcoming events.

### **Step 3: Update Details**
Update times, locations, and status badges as info becomes available.

---

## How to Edit an Event Card

```html
<div class="upcoming-card">
    <div class="upcoming-date">
        <span class="date-month">MAR</span>  <!-- Month (3 letters, uppercase) -->
        <span class="date-day">8</span>       <!-- Day number -->
    </div>
    <div class="upcoming-info">
        <h4>Monthly Mixer</h4>                          <!-- Event name -->
        <p class="event-time">12:00 PM - 4:00 PM</p>   <!-- Time (or "Time TBA") -->
        <p class="event-location">📍 ITP Training Academy</p>  <!-- Location (or "Location TBA") -->
        <span class="event-status status-soon">🔜 Registration Opens Feb 22</span>  <!-- Status -->
    </div>
</div>
```

---

## Status Badge Options

Use ONE of these status classes on `event-status`:

### **1. Tickets/Registration On Sale** (Green/Lime)
```html
<span class="event-status status-onsale">🎫 Tickets On Sale</span>
<span class="event-status status-onsale">📝 Register Now</span>
```

### **2. Coming Soon** (Gold/Orange)
```html
<span class="event-status status-soon">🔜 Registration Opens Soon</span>
<span class="event-status status-soon">🔜 Registration Opens Feb 22</span>
<span class="event-status status-soon">🔜 Tickets Drop Jan 17</span>
```

### **3. Details Coming** (Tan/Neutral)
```html
<span class="event-status status-coming">⏳ Details Coming Soon</span>
<span class="event-status status-coming">📅 Date TBA</span>
```

---

## Example Monthly Updates

### **February 1st Update:**
```
Current:
- Feb 28: Kickoff Party
- Mar 8: Monthly Mixer
- Apr 12: Monthly Mixer

Action: Keep all three (Feb event hasn't happened yet)
```

### **March 1st Update:**
```
Remove:
- Feb 28: Kickoff Party (already happened)

Keep:
- Mar 8: Monthly Mixer
- Apr 12: Monthly Mixer

Add:
- May 10: Monthly Mixer (new)
```

### **April 1st Update:**
```
Remove:
- Mar 8: Monthly Mixer (already happened)

Keep:
- Apr 12: Monthly Mixer
- May 10: Monthly Mixer

Add:
- Jun 14: Monthly Mixer (new)
```

---

## Full Example Update

### Before (End of March):
```html
<div class="upcoming-card">
    <div class="upcoming-date">
        <span class="date-month">MAR</span>
        <span class="date-day">8</span>
    </div>
    <div class="upcoming-info">
        <h4>Monthly Mixer</h4>
        <p class="event-time">12:00 PM - 4:00 PM</p>
        <p class="event-location">📍 ITP Training Academy</p>
        <span class="event-status status-onsale">🎫 Register Now</span>
    </div>
</div>
```

### After (April 1st):
```html
<div class="upcoming-card">
    <div class="upcoming-date">
        <span class="date-month">MAY</span>
        <span class="date-day">10</span>
    </div>
    <div class="upcoming-info">
        <h4>Monthly Mixer</h4>
        <p class="event-time">Time TBA</p>
        <p class="event-location">📍 Location TBA</p>
        <span class="event-status status-coming">⏳ Details Coming Soon</span>
    </div>
</div>
```

---

## Tips for "TBA" Placeholders

Use these when details aren't confirmed yet:

- **Time:** `Time TBA` or `12:00 PM - 4:00 PM` (once confirmed)
- **Location:** `📍 Location TBA` or `📍 ITP Training Academy` (once confirmed)
- **Status:** `⏳ Details Coming Soon` → `🔜 Registration Opens Soon` → `🎫 Register Now`

---

## Event Name Quick Reference

Use consistent naming:

- **Monthly Mixer** (not "Mixer" or "Social Mixer")
- **Sunset Session** (not "Sunset Sessions")
- **Beginner Clinic** (not "Beginners Clinic")
- **Advanced Clinic** (not "Advanced Training")
- **Kickoff Party** (Feb event)
- **Spring Doubles Tournament** (May event)
- **Summer Social Championship** (Aug event)
- **Year-End Awards** (Nov event)

---

## Quick Checklist

Before you push updates:

- [ ] Removed past events
- [ ] Added next event to keep 3 total
- [ ] Updated times if available
- [ ] Updated locations if available
- [ ] Updated status badges appropriately
- [ ] Checked spelling/capitalization
- [ ] Previewed in browser (`preview.html`)

---

## Deploy Updates

```bash
cd /Users/mturner14/Documents/git/tennis-tequila
git add _includes/events.html
git commit -m "Update calendar: [Month] events"
git push
```

Your site will update within a few minutes!

---

## Need Help?

Just copy an existing event card and change the details. It's that simple! 🎾

