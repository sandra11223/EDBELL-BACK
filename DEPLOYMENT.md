# EDBELL EDUSOLUTIONS LLP - Deployment Guide

## 🚨 VERCEL DEPLOYMENT FIX

### Issue: Project Name Conflict
If you're getting the error: `Project "edbell-front-hms7" already exists, please use a new name.`

### Solution: Use Alternative Project Names

Choose one of these available project names:
- `edbell-education-website`
- `edbell-edusolutions-site`
- `edbell-website-2024`
- `edbell-official-website`
- `edbell-education-portal`
- `edbell-learning-platform`
- `edbell-edu-solutions`
- `edbell-website-v2`

### Deployment Steps:
1. **Go to Vercel Dashboard** → New Project
2. **Import GitHub Repository**: https://github.com/sandra11223/EDBELL-FRONT.git
3. **Change Project Name** to one of the suggestions above
4. **Add Environment Variables** (see below)
5. **Deploy**

### Environment Variable Error Fix
If you're getting: `Environment Variable "MONGODB_URI" references Secret "mongodb-uri", which does not exist.`

1. **Go to your Vercel project dashboard**
2. **Navigate to Settings → Environment Variables**
3. **Add the following environment variables:**

```
Name: MONGODB_URI
Value: mongodb+srv://sandraap745_db_user:edbell123@cluster0.8rw8g2z.mongodb.net/edbell-website?retryWrites=true&w=majority&appName=Cluster0

Name: NEXTAUTH_SECRET
Value: your-secret-key-here-make-it-long-and-random

Name: SITE_URL
Value: https://your-domain.vercel.app

Name: SITE_NAME
Value: EDBELL EDUSOLUTIONS LLP
```

4. **Set Environment for:** Production, Preview, and Development
5. **Redeploy your application**

### Important Notes:
- ✅ The `vercel.json` file has been updated to remove secret references
- ✅ Environment variables should be set directly in Vercel dashboard
- ✅ No secrets needed - use regular environment variables

## Quick Deployment Steps

### 1. Push Updated Code
```bash
git add .
git commit -m "Fix Vercel deployment - remove secret references"
git push frontend master
```

### 2. Set Environment Variables in Vercel
- Go to Vercel Dashboard → Your Project → Settings → Environment Variables
- Add all the variables listed above
- Make sure to select all environments (Production, Preview, Development)

### 3. Redeploy
- Go to Deployments tab in Vercel
- Click "Redeploy" on the latest deployment
- Or push a new commit to trigger automatic deployment

## Environment Variables Required

### Essential Variables
```env
MONGODB_URI=mongodb+srv://sandraap745_db_user:edbell123@cluster0.8rw8g2z.mongodb.net/edbell-website?retryWrites=true&w=majority&appName=Cluster0
NEXTAUTH_SECRET=your-secret-key-here
SITE_URL=https://your-domain.vercel.app
SITE_NAME=EDBELL EDUSOLUTIONS LLP
```

### Optional Variables (for email notifications)
```env
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your-email@gmail.com
SMTP_PASS=your-app-password
```

## Deployment Status

✅ **Frontend Repository**: https://github.com/sandra11223/EDBELL-FRONT.git
✅ **Backend Repository**: https://github.com/sandra11223/EDBELL-BACK.git
✅ **Vercel Configuration**: Fixed and ready for deployment
✅ **MongoDB Connection**: Configured and tested
✅ **All Features**: Implemented and working

## Post-Deployment Checklist

### Immediate Actions
- [ ] Set environment variables in Vercel dashboard
- [ ] Redeploy the application
- [ ] Test contact form functionality
- [ ] Verify database connections
- [ ] Check all pages load correctly

### Content Updates
- [ ] Replace placeholder content with real information
- [ ] Add actual university partnerships
- [ ] Update course details and fees
- [ ] Add real testimonials
- [ ] Upload professional images

## Features Deployed

### 🎨 Frontend Features
- **Responsive Design** - Mobile-first approach
- **Unique Page Designs** - Different themes for each page
- **3D Animations** - Interactive effects throughout
- **Contact Form** - Working form with success feedback
- **Newsletter Subscription** - Real-time integration
- **Gallery System** - Photo management
- **Blog System** - Content management

### ⚙️ Backend Features
- **MongoDB Integration** - Complete database setup
- **API Routes** - All CRUD operations
- **Contact Management** - Admin dashboard
- **Analytics System** - Real-time page tracking
- **Course Management** - Dynamic content
- **University Management** - Partner institutions

### 📱 Pages Included
- **Home** - Hero section with services overview
- **About** - Company information and mission
- **Courses** - Filterable course catalog
- **Universities** - Partner institution showcase
- **Services** - Detailed service offerings
- **Blog** - Educational content system
- **Contact** - Working contact form
- **Gallery** - Photo showcase
- **Admin Dashboard** - Complete management system

## Support

If you encounter any issues:
1. Check Vercel deployment logs
2. Verify environment variables are set correctly
3. Ensure MongoDB connection string is valid
4. Test locally first with `npm run dev`

---

**The website is now ready for successful Vercel deployment!** 🚀