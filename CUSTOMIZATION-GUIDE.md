# Portfolio Customization Guide

This guide will help you customize your portfolio website with your own content, images, videos, and audio files.

## 📁 File Structure (Recommended)

Create these folders in your project directory:

```
ced's eporfolio/
├── index.html
├── styles.css
├── README.md
├── CUSTOMIZATION-GUIDE.md
├── images/              (create this folder)
│   ├── banner.jpg
│   ├── profile-photo.jpg
│   ├── project1.jpg
│   ├── project2.jpg
│   ├── gallery1.jpg
│   └── gallery2.jpg
├── videos/              (create this folder)
│   ├── demo1.mp4
│   └── demo2.mp4
└── audio/               (create this folder)
    ├── podcast1.mp3
    └── music.mp3
```

## 🎨 How to Add Your Content

### 1. HOME PAGE - Banner/Background Image

**Option A: Add background image to hero section**

1. Save your banner image as `images/banner.jpg`
2. Open `styles.css`
3. Find the `.hero` section and add:

```css
.hero {
  background-image: url("images/banner.jpg");
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
}
```

**Option B: Add overlay for better text readability**

```css
.hero::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(10, 14, 26, 0.8);
}
```

---

### 2. ABOUT ME PAGE - Profile Photo

Find this in `index.html` (line ~60):

```html
<!-- PLACEHOLDER: Replace with your profile image -->
<div class="image-placeholder">
  <i class="fas fa-user-graduate"></i>
  <p>Add Your Photo Here</p>
</div>
```

**Replace with:**

```html
<img src="images/profile-photo.jpg" alt="Your Name" class="profile-photo" />
```

**Add this CSS to `styles.css`:**

```css
.profile-photo {
  width: 100%;
  max-width: 400px;
  height: 400px;
  object-fit: cover;
  border-radius: 50%;
  border: 5px solid rgba(0, 102, 255, 0.3);
  box-shadow: var(--shadow);
}
```

---

### 3. PROJECTS PAGE - Project Images

Find placeholders like this in `index.html`:

```html
<div class="project-image">
  <i class="fas fa-shopping-cart"></i>
  <p class="placeholder-text">Add Project Image</p>
</div>
```

**Replace with:**

```html
<div class="project-image">
  <img src="images/project1.jpg" alt="Project Name" />
</div>
```

**Or add a video:**

```html
<div class="project-image">
  <video controls poster="images/project1-thumbnail.jpg">
    <source src="videos/project-demo.mp4" type="video/mp4" />
    Your browser does not support video.
  </video>
</div>
```

---

### 4. GALLERY PAGE - Images

Find this in `index.html`:

```html
<div class="gallery-item image-item">
  <i class="fas fa-image"></i>
  <p>Image Placeholder 1</p>
</div>
```

**Replace with:**

```html
<div class="gallery-item">
  <img src="images/gallery1.jpg" alt="Gallery Image 1" />
</div>
```

**Or create a clickable lightbox effect:**

```html
<a href="images/gallery1-full.jpg" target="_blank" class="gallery-item">
  <img src="images/gallery1.jpg" alt="Gallery Image 1" />
</a>
```

---

### 5. GALLERY PAGE - Videos

Find this in `index.html`:

```html
<div class="gallery-item video-item">
  <i class="fas fa-play-circle"></i>
  <p>Video Placeholder 1</p>
</div>
```

**Replace with:**

```html
<video controls width="100%">
  <source src="videos/demo1.mp4" type="video/mp4" />
  Your browser does not support the video tag.
</video>
```

**Or embed YouTube video:**

```html
<iframe
  width="100%"
  height="315"
  src="https://www.youtube.com/embed/YOUR_VIDEO_ID"
  frameborder="0"
  allowfullscreen
>
</iframe>
```

---

### 6. GALLERY PAGE - Audio

Find this in `index.html`:

```html
<div class="gallery-item audio-item">
  <i class="fas fa-volume-up"></i>
  <p>Audio Placeholder 1</p>
</div>
```

**Replace with:**

```html
<audio controls style="width: 100%;">
  <source src="audio/podcast1.mp3" type="audio/mpeg" />
  Your browser does not support the audio tag.
</audio>
```

---

### 7. CONTACT PAGE - Social Media Links

Update the `href="#"` with your actual links:

```html
<!-- GitHub -->
<a href="https://github.com/yourusername" target="_blank">
  <!-- LinkedIn -->
  <a href="https://linkedin.com/in/yourprofile" target="_blank">
    <!-- Facebook -->
    <a href="https://facebook.com/yourprofile" target="_blank">
      <!-- Email -->
      <a href="mailto:c240170@pczc.edu.ph"></a></a></a
></a>
```

---

## 📝 How to Edit Text Content

### Update Your Information:

1. **Name**: Search for "Ced" in `index.html` and replace with your name
2. **Bio**: Update the About Me section paragraph
3. **Education**: Update school names and years
4. **Skills**: Modify the skills list to match your abilities
5. **Projects**: Change project titles, descriptions, and technologies
6. **Contact Info**: Already updated with your email and phone

---

## 🎯 Image Size Recommendations

- **Banner/Hero Background**: 1920x1080px (landscape)
- **Profile Photo**: 400x400px (square)
- **Project Images**: 800x600px (landscape)
- **Gallery Images**: 600x400px or larger
- **Video Thumbnails**: 1280x720px

---

## 🖼️ Image Optimization Tips

1. **Compress images** before uploading (use tools like TinyPNG.com)
2. **Use JPEG** for photos, **PNG** for graphics with transparency
3. **Keep file sizes under 500KB** for faster loading
4. **Use descriptive alt text** for accessibility

---

## 🎬 Video Tips

- **Format**: MP4 (H.264) is most compatible
- **Size**: Keep under 50MB for web
- **Length**: Keep videos under 2 minutes for demos
- **Hosting**: Consider YouTube/Vimeo for large videos

---

## 🔊 Audio Tips

- **Format**: MP3 is most compatible
- **Bitrate**: 128kbps is good for web
- **Keep files under 10MB**

---

## ✅ Testing Checklist

After adding your content:

- [ ] Open `index.html` in a browser
- [ ] Check all images load correctly
- [ ] Test all videos play properly
- [ ] Verify audio files work
- [ ] Click all social media links
- [ ] Test on mobile device (responsive design)
- [ ] Check contact form (note: no backend, just demo)

---

## 🚀 Deployment

Once customized, you can deploy to:

1. **GitHub Pages** (Free)

   - Create a GitHub repository
   - Push your files
   - Enable GitHub Pages in settings

2. **Netlify** (Free)

   - Drag and drop your folder
   - Instant deployment

3. **Vercel** (Free)
   - Connect your GitHub repo
   - Auto-deploy on updates

---

## 💡 Quick Tips

- Create the `images`, `videos`, and `audio` folders before adding files
- Always use **forward slashes** in paths: `images/photo.jpg`
- Test locally before deploying
- Keep backup copies of your files
- Use consistent naming (lowercase, no spaces)

---

## 🆘 Need Help?

Common issues:

- **Image not showing**: Check file path and name spelling
- **Video not playing**: Ensure correct format (MP4)
- **Page looks broken**: Check for missing closing tags in HTML
- **Styles not working**: Verify `styles.css` is in same folder

---

**Good luck with your portfolio! 🎉**
