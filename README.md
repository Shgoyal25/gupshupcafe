# 🍵 GupShup Cafe - Complete Website & Inventory Management System

A modern, fully-featured website and admin dashboard for specialty coffee cafe with comprehensive inventory management, order tracking, and supplier management system.

## ✨ Features

### 🌐 Customer Website
- **Responsive Design**: Works perfectly on mobile, tablet, and desktop
- **Extensive Menu**: 50+ items across multiple categories (Coffee, Tea, Smoothies, Snacks)
- **Online Ordering**: Add items to cart with quantity control
- **User Accounts**: Login and signup functionality
- **Customer Reviews**: Rate and review items and service
- **Location & Hours**: Display cafe information prominently
- **Contact Information**: Phone, email, address, operating hours

### 👨‍💼 Admin Dashboard
- **Inventory Management**: 
  - Add/edit/delete menu items
  - Real-time stock tracking
  - Low stock alerts with visual indicators
  - Automatic reorder notifications
  - Supplier assignment per item

- **Order Management**:
  - View all orders in real-time
  - Order status tracking
  - Customer information
  - Order history and analytics

- **Supplier Management**:
  - Add and manage suppliers
  - Category-wise organization
  - Contact information
  - Delivery timeline tracking
  - Performance analytics

- **Reports & Analytics**:
  - Inventory reports
  - Sales reports
  - Supplier performance
  - Low stock alerts
  - PDF export functionality

- **Settings**:
  - Configurable alert thresholds
  - Notification preferences
  - Email alert configuration

## 📁 File Structure

```
gupshupcafe/
├── index.html              # Main customer website
├── admin.html              # Admin dashboard
├── server.js               # Backend (Node.js) - Optional
├── HOSTING_GUIDE.md        # Comprehensive hosting guide
├── README.md               # This file
└── package.json            # Node.js dependencies
```

## 🚀 Quick Start

### Option 1: Run Locally (Frontend Only)

1. **Download/Clone the project**
```bash
git clone https://github.com/yourusername/gupshupcafe.git
cd gupshupcafe
```

2. **Open in browser**
- Customer Site: Open `index.html` in your browser
- Admin: Open `admin.html` in your browser (use any credentials)

3. **View live**
```bash
# If you have Python 3
python -m http.server 8000

# If you have Python 2
python -m SimpleHTTPServer 8000

# If you have Node.js
npx http-server
```

Visit `http://localhost:8000` in your browser.

### Option 2: Deploy to Netlify (Recommended)

1. Push to GitHub
2. Go to [netlify.com](https://netlify.com)
3. Click "New site from Git"
4. Connect your repository
5. Deploy!

✅ **Your site is live!** (Usually at: `https://yourname.netlify.app`)

## 🔧 Customization Guide

### Update Cafe Information

**In `index.html`**, find and modify:

```html
<!-- Header/Logo -->
<div class="logo">☕ GupShup Cafe</div>

<!-- Hero Section -->
<h1>Welcome to GupShup Cafe</h1>
<p>Premium Coffee & Beverages Crafted with Love</p>

<!-- Contact Section -->
<p>GupShup Cafe, Main Street<br>Your City, State - 000000</p>
<p>+91-9876-543-210</p>

<!-- Operating Hours -->
<p>Mon-Fri: 7:00 AM - 9:00 PM<br>Sat-Sun: 8:00 AM - 10:00 PM</p>
```

### Add/Modify Menu Items

In the JavaScript section of `index.html`, find:

```javascript
const menuItems = [
    { id: 1, name: 'Espresso', category: 'coffee', price: 80, desc: 'Bold and rich', emoji: '☕' },
    // Add more items here...
];
```

Add new items:
```javascript
{ id: 16, name: 'Chocolate Shake', category: 'smoothie', price: 150, desc: 'Rich cocoa delight', emoji: '🥤' },
```

### Change Colors

Update the CSS color scheme:
```css
/* Primary Color (Brown) */
background: linear-gradient(135deg, #8B4513 0%, #D2691E 100%);

/* Accent Color (Gold) */
background: #FFD700;
```

Replace hex colors with your preferred scheme:
- **Orange Accent**: `#FF6B35`
- **Green Accent**: `#52B788`
- **Purple Accent**: `#7209B7`

## 📊 Admin Dashboard Login

**Default Access:**
- Email: (any email)
- Password: (any password)

⚠️ **Before Launch**: Implement proper authentication and security measures (see HOSTING_GUIDE.md)

## 💾 Database & Backend

Currently, the application uses **in-memory storage** (data resets on page refresh).

To persist data, you need:
1. **Backend Server** (Node.js, Python, etc.)
2. **Database** (MySQL, PostgreSQL, MongoDB)

See **HOSTING_GUIDE.md** for complete setup instructions.

## 🌐 Hosting Options

| Option | Cost | Best For | Setup Time |
|--------|------|----------|-----------|
| **Netlify** | FREE | Quick start, small scale | 5 min |
| **AWS Lightsail** | $11/mo | Growing business | 2-4 hrs |
| **DigitalOcean** | $21/mo | More features | 2-4 hrs |
| **Firebase** | FREE-$50/mo | Serverless, scalable | 1-2 hrs |

👉 **Recommendation**: Start with Netlify, migrate to AWS Lightsail when you're ready for a real database.

## 🔐 Security Checklist

- [ ] Change admin login mechanism
- [ ] Use environment variables for secrets
- [ ] Enable HTTPS on production
- [ ] Implement rate limiting
- [ ] Validate all user inputs
- [ ] Secure API endpoints
- [ ] Regular backups
- [ ] Monitor error logs
- [ ] Use strong passwords

See HOSTING_GUIDE.md for security best practices.

## 🎨 Customization Examples

### Change Cafe Color Scheme
```css
/* In index.html, find and update */
background: linear-gradient(135deg, YOUR_COLOR1 0%, YOUR_COLOR2 100%);
```

### Add Social Media Links
```html
<!-- In footer -->
<a href="https://instagram.com/gupshup.cafe">Instagram</a>
<a href="https://facebook.com/gupshup.cafe">Facebook</a>
```

### Add WhatsApp Order Button
```html
<a href="https://wa.me/919876543210?text=Hi%2C%20I%20want%20to%20order">
  <button class="btn btn-primary">Order on WhatsApp</button>
</a>
```

### Integrate Google Maps
```html
<iframe src="https://www.google.com/maps/embed?pb=YOUR_EMBED_CODE" 
        width="100%" height="400" style="border:0;" 
        allowfullscreen="" loading="lazy"></iframe>
```

## 📱 Mobile Optimization

The website is fully responsive. Test on:
- iPhone 12/13
- Android phones
- iPad
- Desktop screens

All elements adapt automatically.

## 📈 Analytics Integration

Add Google Analytics:
```html
<!-- Add before </head> -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>
```

## 🚀 Future Enhancements

1. **Payment Integration** (Razorpay, PayPal)
2. **Email Notifications** (SendGrid, Gmail)
3. **SMS Alerts** (Twiglio for order updates)
4. **Real-time Inventory Sync** (WebSockets)
5. **Customer Loyalty Program**
6. **Mobile App** (React Native)
7. **Multi-location Support**
8. **Staff Management System**
9. **Table Reservation System**
10. **Delivery Integration** (Zomato, Swiggy API)

## 📞 Support & Documentation

- **HOSTING_GUIDE.md**: Complete hosting & deployment guide
- **Admin Guide**: Inventory management tutorials (coming soon)
- **API Documentation**: (coming soon)
- **FAQ**: (coming soon)

## 🤝 Contributing

Want to improve the application?
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📄 License

This project is open-source. Feel free to use, modify, and distribute.

## ✅ Pre-Launch Checklist

- [ ] Customize cafe information
- [ ] Upload actual menu items
- [ ] Set up admin credentials
- [ ] Test all features
- [ ] Optimize images
- [ ] Set up domain name
- [ ] Configure SSL/HTTPS
- [ ] Implement payment gateway
- [ ] Set up backup system
- [ ] Create admin documentation
- [ ] Test on mobile devices
- [ ] Launch!

## 🎯 Quick Tips

1. **First Time?** Start with Netlify (it's free!)
2. **Growing Business?** Upgrade to AWS Lightsail
3. **Need Help?** Check HOSTING_GUIDE.md
4. **Want Real Database?** Follow backend setup in HOSTING_GUIDE.md
5. **Security First?** Review security checklist before going live

## 📊 Next Steps

1. **This Week**: Deploy to Netlify & test
2. **Next Week**: Customize with your menu & info
3. **Week 3**: Set up payment & customer accounts
4. **Week 4**: Launch publicly & monitor

---

**Created for**: GupShup Cafe, Dehradun  
**Version**: 1.0  
**Last Updated**: January 2024

**Questions?** Reach out to the development team or check HOSTING_GUIDE.md for comprehensive documentation.

---

### 🌟 Built with ☕ and 💙
