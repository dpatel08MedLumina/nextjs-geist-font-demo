# MedLumina Customization Guide

This guide will help you customize the MedLumina website to add your personal information and make other modifications.

## 🎯 Key Files to Edit

### 1. **Homepage** (`src/app/page.tsx`)
This is the main landing page where you can add your personal story and customize the hero section.

**What you can customize:**
- Hero section title and description
- Your personal story in the "Why MedLumina?" section
- Call-to-action buttons
- Feature descriptions

**Example changes:**
```tsx
// Change the hero section
<h1 className="text-4xl md:text-6xl font-bold text-gray-900 mb-6">
  Welcome to <span className="text-blue-600">MedLumina</span>
</h1>
<p className="text-xl md:text-2xl text-gray-700 mb-8 max-w-3xl mx-auto">
  Hi! I'm [Your Name], and I created this platform to help high school students 
  like you navigate the path to healthcare careers. Having gone through this 
  journey myself, I understand the challenges and want to share what I've learned.
</p>
```

### 2. **Site Layout & Navigation** (`src/app/layout.tsx`)
Controls the overall site structure, navigation, and footer.

**What you can customize:**
- Site title and description
- Navigation menu items
- Footer content with your contact information
- Add your social media links

**Example changes:**
```tsx
// Update metadata
export const metadata: Metadata = {
  title: 'MedLumina - [Your Name]\'s Healthcare Career Platform',
  description: 'Created by [Your Name] to help students pursue healthcare careers',
}

// Add your info to footer
<div>
  <h3 className="text-lg font-semibold text-gray-900 mb-4">About the Creator</h3>
  <p className="text-gray-600 text-sm">
    Created by [Your Name], a [Your Background] passionate about helping 
    students succeed in healthcare careers.
  </p>
  <p className="text-gray-600 text-sm mt-2">
    Contact: [your.email@example.com]
  </p>
</div>
```

### 3. **About Section** (Create new page: `src/app/about/page.tsx`)
Add a dedicated page about yourself and your mission.

## 🛠️ How to Make Changes

### Step 1: Edit Text Content
1. Open any `.tsx` file in the `src/app/` directory
2. Look for text between `>` and `<` tags
3. Replace with your own content
4. Save the file

### Step 2: Add Your Personal Story
Create an About page by adding this file: `src/app/about/page.tsx`

### Step 3: Update Contact Information
1. Edit `src/app/layout.tsx` 
2. Find the footer section
3. Replace placeholder contact info with yours

### Step 4: Customize Colors and Styling
1. Edit `src/app/globals.css` for global color changes
2. Or modify individual components by changing Tailwind classes

## 📝 Common Customizations

### Add Your Photo
1. Add your photo to the `public/` folder
2. Reference it in components like: `<img src="/your-photo.jpg" alt="Your Name" />`

### Change the Site Name
1. Update `layout.tsx` metadata
2. Update the header logo text
3. Update page titles throughout the site

### Add Your Social Media
```tsx
// In layout.tsx footer
<div className="flex space-x-4">
  <a href="https://linkedin.com/in/yourprofile" className="text-gray-600 hover:text-gray-900">
    LinkedIn
  </a>
  <a href="https://twitter.com/yourhandle" className="text-gray-600 hover:text-gray-900">
    Twitter
  </a>
</div>
```

### Customize Sample Data
Replace the sample data in each page with your own:
- Mentor profiles with people you know
- Project ideas you've worked on
- Events you've attended or organized
- Scholarships you've received

## 🚀 Testing Your Changes

1. Run `npm run dev` in your terminal
2. Open `http://localhost:8000` in your browser
3. Navigate through the site to see your changes
4. Make additional edits as needed

## 📁 File Structure Quick Reference

```
src/app/
├── page.tsx                    # Homepage
├── layout.tsx                  # Site layout & navigation
├── field-circles/page.tsx      # Healthcare forums
├── extracurricular-ideas/page.tsx  # Project ideas
├── applications-archive/page.tsx   # Application materials
├── mentor-match/page.tsx       # Mentor connections
├── live-events/page.tsx        # Events & webinars
├── college-match/page.tsx      # College recommendations
├── project-collaboration/page.tsx  # Team projects
└── scholarships/page.tsx       # Funding opportunities
```

## 💡 Pro Tips

1. **Start Small**: Make one change at a time and test it
2. **Keep Backups**: Save copies of original files before major changes
3. **Use Search & Replace**: Use your editor's find/replace to change text across multiple files
4. **Test on Mobile**: Check how your changes look on different screen sizes
5. **Ask for Help**: If you get stuck, the error messages usually tell you what's wrong

## 🎨 Design Customization

The site uses Tailwind CSS for styling. You can:
- Change colors by modifying class names like `text-blue-600` to `text-green-600`
- Adjust spacing with classes like `mb-4` (margin-bottom) or `p-6` (padding)
- Modify layouts with classes like `grid-cols-2` or `flex-col`

Remember: Every change you make will be reflected immediately when you save the file (if the dev server is running)!
