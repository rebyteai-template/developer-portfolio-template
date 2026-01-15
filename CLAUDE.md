# AI Agent Instructions for Developer Portfolio Template

This file provides guidance for AI coding agents customizing this Next.js portfolio template.

## Quick Start

1. **Personal Info**: Edit `utils/data/personal-data.js` for name, bio, skills
2. **Projects**: Edit `utils/data/projects.js` for project showcase
3. **Experience**: Edit `utils/data/experience.js` for work history
4. **Homepage**: Edit `app/page.js` for layout customization

---

## Files to MODIFY (Customize These)

### Personal Data (Most Important)
| File | Purpose |
|------|---------|
| `utils/data/personal-data.js` | Name, title, bio, social links, skills |
| `utils/data/projects.js` | Project showcase with images and links |
| `utils/data/experience.js` | Work experience timeline |
| `utils/data/educations.js` | Education history |

### Pages
| File | Purpose |
|------|---------|
| `app/page.js` | Homepage layout |
| `app/blog/page.js` | Blog listing |

### Assets
| Location | Purpose |
|----------|---------|
| `public/` | Images, resume PDF, favicon |

### Styling
| File | Purpose |
|------|---------|
| `tailwind.config.js` | Theme colors and customization |

---

## Files to KEEP (Don't Modify Unless Necessary)

```
app/components/    # Reusable UI components
app/api/          # API routes (contact form)
utils/            # Utility functions (except data files)
```

---

## Data File Structures

### personal-data.js
```javascript
export const personalData = {
  name: "Your Name",              // CHANGE THIS
  profile: '/profile.png',        // Add your photo to public/
  designation: "Software Developer",
  description: "Your bio...",
  email: 'your@email.com',
  phone: '+1234567890',
  address: 'Your City, Country',
  github: 'https://github.com/yourusername',
  linkedIn: 'https://linkedin.com/in/yourusername',
  twitter: 'https://twitter.com/yourusername',
  devUsername: "yourusername",    // Dev.to username
  resume: "/resume.pdf"           // Add your resume to public/
};
```

### projects.js
```javascript
export const projectsData = [
  {
    id: 1,
    name: 'Project Name',
    description: "Project description...",
    tools: ['React', 'Node.js', 'MongoDB'],
    role: 'Full Stack Developer',
    code: 'https://github.com/...',
    demo: 'https://demo-url.com',
    image: '/projects/project1.png',  // Add to public/projects/
  },
  // Add more projects...
];
```

---

## Environment Variables

Create `.env.local` from `.env.example`:

```env
# Required for contact form
NEXT_PUBLIC_EMAILJS_SERVICE_ID=your_service_id
NEXT_PUBLIC_EMAILJS_TEMPLATE_ID=your_template_id
NEXT_PUBLIC_EMAILJS_PUBLIC_KEY=your_public_key

# Google reCAPTCHA (optional)
NEXT_PUBLIC_RECAPTCHA_SITE_KEY=your_site_key
RECAPTCHA_SECRET_KEY=your_secret_key

# Google Analytics (optional)
NEXT_PUBLIC_GTM=GTM-XXXXXXX
```

---

## Icons

This template uses `react-icons`. Available icon sets:
- `Fa*` - Font Awesome
- `Si*` - Simple Icons (brand logos)
- `Md*` - Material Design
- `Bs*` - Bootstrap Icons

Example usage:
```jsx
import { FaGithub, SiReact } from 'react-icons/fa';
<FaGithub className="w-6 h-6" />
```

---

## Build and Test

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Start production server
npm run start
```

---

## Deployment Notes

This is a Next.js app. For static export:

```javascript
// next.config.js
module.exports = {
  output: 'export',
  images: { unoptimized: true }
};
```

Then run `npm run build` - output goes to `out/` folder.
