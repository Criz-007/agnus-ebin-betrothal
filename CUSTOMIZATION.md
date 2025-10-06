# Customization Guide

This guide will help you customize the Add-to-Calendar page for your own event.

## Event Details

To change the event details, open `index.html` and locate the `eventDetails` object in the `<script>` section (around line 232):

```javascript
const eventDetails = {
    title: "Agnus & Ebin Betrothal",
    description: "Join us to celebrate the betrothal of Agnus & Ebin. We look forward to sharing this special moment with you!",
    location: "To be announced",
    startDate: new Date("2025-01-26T10:00:00"),
    endDate: new Date("2025-01-26T12:00:00")
};
```

### Fields to Customize:

1. **title** - The name of your event
2. **description** - A brief description of your event
3. **location** - The venue or address of your event
4. **startDate** - When your event starts (format: YYYY-MM-DDTHH:mm:ss)
5. **endDate** - When your event ends (format: YYYY-MM-DDTHH:mm:ss)

### Date Format

The date should be in ISO format without timezone (local time):
- `new Date("2025-01-26T10:00:00")` means January 26, 2025 at 10:00 AM

## Display Text

To change the text shown on the page, update these HTML elements:

### Page Title and Heading
```html
<h1>💍 Agnus & Ebin 💍</h1>
<p class="subtitle">Betrothal Ceremony</p>
```

### Event Details Display
Find the elements with these IDs and update the text:
- `id="event-date"` - The displayed date
- `id="event-time"` - The displayed time
- `id="event-location"` - The displayed location
- `id="event-description"` - The displayed description

Example:
```html
<span id="event-date">Sunday, January 26, 2025</span>
```

## Styling

### Colors
The page uses a gradient background. To change colors, modify the CSS in the `<style>` section:

```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Button Colors
Each calendar button has its own class. Find and modify:
- `.btn-google` - Google Calendar button (default: blue)
- `.btn-apple` - Apple Calendar button (default: dark gray)
- `.btn-outlook` - Outlook button (default: blue)
- `.btn-yahoo` - Yahoo Calendar button (default: purple)
- `.btn-office365` - Office 365 button (default: orange)

## Adding More Calendar Services

To add support for additional calendar services, you'll need to:

1. Add a new button in the HTML
2. Create a function to generate the calendar URL
3. Set the button's href in the JavaScript

Example for adding a new service:

```html
<!-- Add button -->
<a href="#" class="calendar-btn btn-newservice" id="btn-newservice">
    New Service
</a>
```

```javascript
// Add function
function getNewServiceUrl() {
    // Generate URL based on service's API
    return "https://newservice.com/calendar/add?...";
}

// Set the link
document.getElementById('btn-newservice').href = getNewServiceUrl();
```

## Testing Your Changes

After making changes:

1. Open `index.html` in your web browser
2. Click each calendar button to verify the links work
3. Check that the event details are correct in each calendar service

## Deployment

Once customized, you can deploy the page to:

- **GitHub Pages**: Enable in repository settings
- **Netlify**: Drag and drop the `index.html` file
- **Vercel**: Connect your repository
- **Any web hosting**: Upload the `index.html` file

## Need Help?

If you encounter any issues:

1. Check the browser console for JavaScript errors (F12 in most browsers)
2. Verify your date format is correct
3. Make sure all quotes and brackets are properly closed
4. Test the page locally before deploying

## Example: Wedding Event

Here's an example customization for a wedding:

```javascript
const eventDetails = {
    title: "John & Jane Wedding",
    description: "Join us for our special day! Reception to follow ceremony.",
    location: "St. Mary's Church, 123 Main Street, New York, NY",
    startDate: new Date("2025-06-15T14:00:00"),
    endDate: new Date("2025-06-15T22:00:00")
};
```

```html
<h1>💒 John & Jane 💒</h1>
<p class="subtitle">Wedding Celebration</p>
```

Enjoy your customized Add-to-Calendar page!
