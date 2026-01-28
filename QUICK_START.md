# Quick Start Guide 🚀

## In 3 Steps

### Step 1: Start Your Server
```bash
node server.js
```
✅ Server runs at http://localhost:3000

### Step 2: Upload Your Products
1. Open http://localhost:3000/admin.html
2. Login: **admin** / **admin**
3. Click "Add Product"
4. Pick image from your computer
5. Fill details (name, price, category)
6. Click "Save Product"

### Step 3: View on Website
- Open http://localhost:3000
- Your products appear immediately!
- No hardcoded items
- Only YOUR uploads show

---

## ✅ What's Fixed

| Issue | Before | After |
|-------|--------|-------|
| **Picture Upload** | ❌ Failed | ✅ Works perfectly |
| **Hardcoded Products** | ❌ 20 demo items | ✅ None - only your uploads |
| **Product Updates** | ❌ Required refresh | ✅ Real-time automatic |
| **Image Storage** | ❌ Lost on reload | ✅ Saved permanently |

---

## Key Features Now Working

✅ Upload product pictures from your computer  
✅ Only see YOUR products (no demo items)  
✅ Products update instantly  
✅ Images stored on server  
✅ Edit/delete products anytime  
✅ Customers can browse & order  

---

## File Locations

```
admin.html        → Upload products here
index-1.html      → Customer sees this
server.js         → Runs the server
data/products.json    → Your products stored here
uploads/          → Your product images here
```

---

## Common Tasks

**Add a Product:**
1. Admin panel → "Add Product"
2. Pick image → Fill form → Save

**Edit a Product:**
1. Admin panel → Click "Edit" → Update → Save

**Delete a Product:**
1. Admin panel → Click "Delete" → Confirm

**See Products:**
1. Refresh website (or wait 1 second)
2. Products show under right category

---

## Troubleshooting

**Server won't start?**
```bash
npm install    # Install dependencies
node server.js # Try again
```

**Images not uploading?**
- Check file size (max 10MB)
- Try JPG or PNG format
- Refresh browser page

**Products not showing?**
- Refresh website (Ctrl+F5)
- Check if server is running
- Look at browser console (F12)

---

## That's It! 🎉

Your system is ready to use!

- No more hardcoded products
- Pictures upload perfectly
- Everything is permanent
- Customers see only your items

**Questions?** Check UPLOAD_FIX_GUIDE.md for details.
