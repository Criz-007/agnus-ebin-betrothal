# Agnus & Ebin Betrothal

Add-to-Calendar page for the Betrothal of Agnus & Ebin.

## 🎉 About

This is a simple, elegant web page that allows guests to add the Agnus & Ebin Betrothal event to their calendar with a single click. The page supports multiple calendar services including Google Calendar, Apple Calendar, Outlook, Yahoo Calendar, and Office 365.

## 🚀 Usage

Simply open `index.html` in a web browser or deploy it to any web hosting service. Guests can then click on their preferred calendar service button to add the event.

### Supported Calendar Services

- **Google Calendar** - Opens Google Calendar with pre-filled event details
- **Apple Calendar** - Downloads an ICS file that can be opened in Apple Calendar
- **Outlook** - Downloads an ICS file compatible with Outlook
- **Yahoo Calendar** - Opens Yahoo Calendar with pre-filled event details
- **Office 365** - Opens Office 365 Calendar with pre-filled event details

## ⚙️ Customization

To customize the event details, edit the `eventDetails` object in the `<script>` section of `index.html`:

```javascript
const eventDetails = {
    title: "Agnus & Ebin Betrothal",
    description: "Join us to celebrate the betrothal of Agnus & Ebin. We look forward to sharing this special moment with you!",
    location: "To be announced",
    startDate: new Date("2025-01-26T10:00:00"),
    endDate: new Date("2025-01-26T12:00:00")
};
```

You can also update the display values in the HTML section if needed.

## 📱 Features

- ✅ Responsive design that works on mobile and desktop
- ✅ Beautiful gradient background with clean UI
- ✅ Support for all major calendar services
- ✅ ICS file generation for Apple Calendar and Outlook
- ✅ Direct links for Google Calendar, Yahoo, and Office 365
- ✅ Clear instructions for users
- ✅ Event details prominently displayed

## 🌐 Deployment

You can deploy this page to:
- GitHub Pages
- Netlify
- Vercel
- Any static web hosting service

Simply upload the `index.html` file or push it to your repository and enable GitHub Pages.

## 📸 Preview

![Betrothal Calendar Page](https://github.com/user-attachments/assets/95465ba2-656c-40d9-b4e7-0653e50a3e80)

## 📝 License

Free to use for personal events.