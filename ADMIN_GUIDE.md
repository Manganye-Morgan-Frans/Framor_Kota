# 🔐 Framor Kotas Admin Panel - User Guide

## 📋 Overview
The admin panel is a fully functional product management system that allows you to add, edit, and delete products. All changes are automatically synchronized with the main website (index-1.html).

---

## 🔑 Login Credentials
- **Username:** `admin`
- **Password:** `admin`

> **Security Note:** For production use, update these credentials and implement proper backend authentication.

---

## 📍 Accessing the Admin Panel

### Method 1: Direct Link
Go to: `admin.html` in your browser

### Method 2: From Website
- Open `index-1.html`
- Click the **"Admin"** button in the top navigation bar (next to the cart)

---

## ✨ Admin Panel Features

### 1. **Dashboard Overview**
When you log in, you'll see:
- **Total Products** - Count of all products (default + admin-added)
- **Bestsellers** - Products marked with "Bestseller" badge
- **New Products** - Products marked with "New" badge
- **Popular Items** - Products marked with "Popular" badge

### 2. **Add Products**
Click **"+ Add Product"** button to add new items:

**Fields to fill:**
- **Product Name** - Name of the product (e.g., "Deluxe Kota")
- **Category** - Choose from:
  - Kota & Chips
  - Drinks
  - Burgers
  - Pizzas
  - Snacks
- **Price** - Product price in Rand (R)
- **Badge** - Optional badge (Bestseller, New, Popular, or None)
- **Description** - Product description (e.g., "Delicious kota with special sauce")

Click **"Save Product"** to add it.

### 3. **Edit Products**
- Click the **"Edit"** button next to any product
- Modify the details
- Click **"Save Product"** to update

### 4. **Delete Products**
- Click the **"Delete"** button next to any product
- Confirm the deletion (this action cannot be undone)

### 5. **Filter & Search**
**Search Bar:**
- Type in the search box to find products by name or description

**Filter by Category:**
- Click on category buttons (All, Kota & Chips, Drinks, Burgers, Pizzas, Snacks)
- Only products in that category will be displayed

**Filter by Badge:**
- Click on badge buttons (Bestseller, New, Popular)
- See only products with that badge

---

## 🎯 How It Works

### Data Storage
- Products are stored in **Browser LocalStorage** (`frameorKotasProducts`)
- Data persists even after closing the browser
- Each browser/device has its own storage

### Synchronization
1. **Admin adds/edits products** → Saved to LocalStorage
2. **Website loads** → Automatically fetches admin products
3. **Website displays** → Default products + Admin products together
4. **Customers order** → Works seamlessly with both types of products

### Product IDs
- **Default products:** IDs 1-20
- **Admin products:** IDs 21+ (auto-generated)
- Each product has a unique ID

---

## 📊 Product Statistics

The dashboard shows real-time statistics:
- Updates automatically when you add/edit/delete products
- Counts products by badges (Bestseller, New, Popular)
- Displays total number of products

---

## 🔄 Workflow Example

### Adding a Custom Product:
1. Login to admin panel
2. Click **"+ Add Product"**
3. Fill in details:
   - Name: "Grilled Chicken Kota"
   - Category: "Kota & Chips"
   - Price: "58.00"
   - Badge: "New"
   - Description: "Juicy grilled chicken with fresh veggies"
4. Click **"Save Product"**
5. Visit `index-1.html` → Your product appears under "Kota & Chips"
6. Customers can add it to their cart and order!

---

## 🎨 Features Included

✅ **Beautiful Dashboard UI**
- Modern, responsive design
- Smooth animations and transitions
- Color-coded badges
- Mobile-friendly interface

✅ **Full CRUD Operations**
- Create (Add new products)
- Read (View all products)
- Update (Edit products)
- Delete (Remove products)

✅ **Advanced Filtering**
- Search by product name or description
- Filter by category
- Filter by badge status
- Real-time results

✅ **Data Management**
- Add unlimited products
- Edit existing products
- Delete unwanted products
- Automatic ID generation

✅ **Real-time Sync**
- Changes appear instantly on the website
- No page refresh needed for website
- LocalStorage persistence

---

## 📱 Mobile Support

The admin panel is fully responsive:
- **Desktop:** Full feature set with all sidebars
- **Tablet:** Optimized layout
- **Mobile:** Vertical layout with collapsible sections

---

## 🔒 Security Notes

### Current Security:
- Login via username/password (client-side)
- Session stored in browser sessionStorage
- Logout clears the session

### For Production:
1. Update default credentials
2. Implement backend authentication
3. Use HTTPS for all connections
4. Add database instead of LocalStorage
5. Add role-based permissions
6. Implement audit logging

---

## ⚠️ Important Notes

### Data Backup:
- Products are stored locally in the browser
- Clear browser data/cache will delete all admin products
- **Backup important data manually** before clearing browser data

### Best Practices:
1. Keep default products (1-20) for reference
2. Use clear, descriptive product names
3. Set appropriate prices with decimals (e.g., 45.00)
4. Use badges strategically (not on every product)
5. Write helpful product descriptions

### Troubleshooting:
- **Admin page won't load?** - Check if JavaScript is enabled
- **Products not appearing?** - Refresh the website (index-1.html)
- **Lost password?** - Update credentials in admin.html line ~225-226
- **Clear all products?** - Delete them manually or clear browser storage

---

## 🚀 Next Steps

After setting up products:
1. ✅ Add your signature products
2. ✅ Mark bestsellers with "Bestseller" badge
3. ✅ Highlight new items with "New" badge
4. ✅ Feature popular items with "Popular" badge
5. ✅ Test ordering on the website
6. ✅ Share admin.html link with team members
7. ✅ Keep updating products regularly

---

## 📞 Support

If you need help:
- Check that you're using correct login credentials
- Ensure JavaScript is enabled in your browser
- Try opening the admin panel in an incognito/private window
- Make sure you're accessing the correct admin.html file

---

**Happy Product Management! 🎉**

Your Framor Kotas Admin Panel is ready to use. Start adding amazing products and delight your customers!
