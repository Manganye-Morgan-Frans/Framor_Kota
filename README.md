# Framor Kotas Admin Panel - Setup Guide

## What's Fixed

✅ **Unlimited Image Uploads** - No more storage limits (previously limited by localStorage)  
✅ **Cross-Device Persistence** - Products and images persist across all devices  
✅ **Reliable Storage** - Files are saved on the server, not limited to browser cache  
✅ **Larger File Support** - Now supports up to 10MB per image (previously 2MB)

## How It Works

The system now uses:
- **Backend Server**: Node.js/Express for handling uploads and data management
- **File Storage**: Images stored as actual files on the server (not base64)
- **Database**: JSON file-based database for product information
- **Persistent Storage**: All data remains even after closing/reopening the browser

## Installation & Setup

### Step 1: Install Node.js
Download and install Node.js from: https://nodejs.org/ (choose LTS version)

### Step 2: Install Dependencies
Open PowerShell/Command Prompt in the `Errol 2 kota` folder and run:

```
npm install
```

This will install Express, Multer, and CORS dependencies.

### Step 3: Start the Server
Run the server:

```
npm start
```

You should see:
```
Server running at http://localhost:3000
Uploads directory: D:\...\uploads
Data directory: D:\...\data
```

### Step 4: Open Admin Panel
Open `admin.html` in your browser. The app will automatically connect to the server at `http://localhost:3000`

**Default Login:**
- Username: `admin`
- Password: `admin`

## Folder Structure

```
Errol 2 kota/
├── admin.html           (The admin dashboard)
├── server.js            (Backend server)
├── package.json         (Dependencies)
├── uploads/             (Stores product images)
└── data/
    └── products.json    (Stores product information)
```

## Features

✨ **Unlimited Uploads** - Add as many products as you want  
🖼️ **Image Support** - JPG, PNG, GIF (up to 10MB each)  
🌍 **Multi-Device Access** - Same data on any device accessing the server  
⚡ **Fast Performance** - Images stored as files, not as base64  
🔒 **Secure** - Login protection for admin panel  

## Using the Admin Panel

1. **Add Product**
   - Click "Add Product" button
   - Fill in product details
   - Upload an image (optional)
   - Click "Save Product"

2. **View Products**
   - All products appear in the list
   - Use filters to search by category or badge

3. **Edit Product**
   - Click "Edit" on any product
   - Modify details or upload a new image
   - Click "Save Product"

4. **Delete Product**
   - Click "Delete" to remove a product
   - Confirm the deletion

## Accessing from Another Device

To access the admin panel from another computer/device on your network:

1. Find your computer's IP address (run `ipconfig` in PowerShell)
2. On another device, go to: `http://YOUR_IP:3000/admin.html`
   - Example: `http://192.168.1.100:3000/admin.html`

## Troubleshooting

**Issue: "Connection refused"**
- Make sure the server is running (`npm start`)
- Check that port 3000 is not blocked by firewall

**Issue: Images not uploading**
- Make sure the `uploads` folder exists (created automatically)
- Check file size is less than 10MB
- Check image format (JPG, PNG, GIF supported)

**Issue: Products not saving**
- Ensure `data` folder exists (created automatically)
- Check file permissions on the folders
- Check browser console for error messages (F12)

## Development

To use auto-reload during development:

```
npm install nodemon --save-dev
npm run dev
```

## Important Notes

⚠️ **Keep the Server Running** - The admin panel requires the server to be active  
⚠️ **Network Access** - Ensure other devices can reach your IP:port  
⚠️ **Firewall** - You may need to allow Node.js through your firewall  

## API Endpoints (For Reference)

- `GET /api/products` - Get all products
- `POST /api/products` - Add new product (with image upload)
- `PUT /api/products/:id` - Update product
- `DELETE /api/products/:id` - Delete product
- `GET /uploads/:filename` - Access product images

---

**Questions or Issues?** Check that:
1. Node.js is installed correctly
2. Dependencies are installed (`npm install`)
3. Server is running without errors
4. Browser can access `http://localhost:3000/api/products`
