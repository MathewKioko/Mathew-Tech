# MathewTech - Premium Personal Brand Website

A production-ready personal brand website built with Next.js 14, TypeScript, Tailwind CSS, and Framer Motion. Features premium dark theme design with gold accents, GitHub API integration, and EmailJS contact form.

![MathewTech](https://img.shields.io/badge/Next.js-14-black) ![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue) ![Tailwind](https://img.shields.io/badge/Tailwind-3.4-cyan)

## Live Demo

🔗 https://mathew-tech.vercel.app/

📂 **GitHub Repository**: https://github.com/MathewKioko/MathewTech

## Features

### Core Features
- 🎨 Premium dark theme with gold accents
- 📱 Fully responsive (mobile-first design)
- ✨ Smooth animations with Framer Motion
- 🔧 GitHub API integration for projects
- 📧 EmailJS contact form with validation
- 📜 Scroll progress indicator
- 🎯 SEO optimized with metadata

### Sections
1. **Navbar** - Sticky navigation with mobile hamburger menu
2. **Hero** - Animated introduction with logo showcase
3. **About** - Timeline and skills showcase
4. **Services** - 6 service cards with hover effects
5. **Projects** - GitHub repo integration with filtering
6. **Contact** - Form with EmailJS integration
7. **Footer** - Navigation and social links

## Tech Stack

- **Framework:** Next.js 14 (App Router)
- **Language:** TypeScript
- **Styling:** Tailwind CSS
- **Animations:** Framer Motion
- **Icons:** React Icons
- **Email:** EmailJS
- **Deployment:** Vercel

## Getting Started

### Prerequisites

- Node.js 18+ installed
- npm or yarn package manager
- Git for version control

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd mathewtech
```

2. Install dependencies:
```bash
npm install
```

3. Copy environment variables:
```bash
cp .env.local.example .env.local
```

4. Add your configuration to `.env.local`:
```env
NEXT_PUBLIC_EMAILJS_SERVICE_ID=your_service_id
NEXT_PUBLIC_EMAILJS_TEMPLATE_ID=your_template_id
NEXT_PUBLIC_EMAILJS_PUBLIC_KEY=your_public_key
```

5. Run development server:
```bash
npm run dev
```

6. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Project Structure

```
mathewtech/
├── app/
│   ├── layout.tsx          # Root layout with metadata
│   ├── page.tsx            # Main page
│   └── globals.css         # Global styles
├── components/
│   ├── Navbar.tsx          # Navigation component
│   ├── Footer.tsx          # Footer component
│   └── ScrollProgress.tsx  # Scroll progress bar
├── sections/
│   ├── Hero.tsx            # Hero section
│   ├── About.tsx           # About section with timeline
│   ├── Services.tsx        # Services section
│   ├── Projects.tsx        # GitHub projects section
│   └── Contact.tsx         # Contact form section
├── lib/
│   └── utils.ts            # Utility functions
├── types/
│   └── index.ts            # TypeScript interfaces
├── public/
│   ├── logo.png            # Site logo
│   ├── favicon.ico         # Favicon
│   └── resume.pdf          # Resume file (optional)
├── .env.local.example      # Environment variables template
├── tailwind.config.ts      # Tailwind configuration
├── next.config.js          # Next.js configuration
└── package.json            # Dependencies
```

## GitHub API Integration

### How It Works

The Projects section fetches repositories from GitHub using the REST API:

1. **API Endpoint:** `https://api.github.com/users/{username}/repos`
2. **Features:**
   - Fetches user's public repositories
   - Filters out forked repositories
   - Sorts by most recently updated
   - Filters by programming language
   - Displays: name, description, language, stars, last updated

### Configuration

In `sections/Projects.tsx`, change the username:
```typescript
const GITHUB_USERNAME = "delvis007"; // Change to your GitHub username
```

### Rate Limits

- **Unauthenticated:** 60 requests/hour
- **Authenticated:** 5,000 requests/hour

To increase limits, add a GitHub token:
```env
GITHUB_TOKEN=your_github_token
```

## EmailJS Setup

### 1. Create EmailJS Account
1. Go to [EmailJS](https://www.emailjs.com/)
2. Sign up for free account
3. Verify your email

### 2. Create Email Service
1. Click "Email Services" → "Add New Service"
2. Choose your email provider (Gmail, Outlook, etc.)
3. Connect your email account
4. Note the **Service ID**

### 3. Create Email Template
1. Click "Email Templates" → "Create New Template"
2. Design your email template
3. Use variables: `{{name}}`, `{{email}}`, `{{message}}`
4. Save and note the **Template ID**

### 4. Get Public Key
1. Click "Account" → "API Key"
2. Note your **Public Key**

### 5. Configure Environment
```env
NEXT_PUBLIC_EMAILJS_SERVICE_ID=service_xxxxx
NEXT_PUBLIC_EMAILJS_TEMPLATE_ID=template_xxxxx
NEXT_PUBLIC_EMAILJS_PUBLIC_KEY=public_xxxxx
```

## Deployment

### Vercel (Recommended)

1. **Push to GitHub:**
```bash
git add .
git commit -m "Initial commit"
git push origin main
```

2. **Deploy on Vercel:**
   - Go to [Vercel](https://vercel.com)
   - Sign in with GitHub
   - Click "New Project"
   - Import your repository
   - Add environment variables
   - Click "Deploy"

3. **Your site will be live at:** `https://mathewtech.vercel.app`

### Build for Production

```bash
npm run build
npm start
```

## Customization

### Colors

Edit `tailwind.config.ts`:
```typescript
colors: {
  accent: {
    gold: "#C9A227",      // Primary accent
    green: "#006B3C",     // Secondary
    orange: "#A44C0F",    // Tertiary
  },
}
```

### Update Links

Search and replace these in the project:
- `delvis007` - GitHub username
- `delvis-kioko` - LinkedIn username
- `delviskioko@example.com` - Your email
- `254700000000` - WhatsApp number

### Add Resume

1. Add your PDF to `public/resume.pdf`
2. The download button in Hero will work automatically

## Performance

- Lighthouse Score: 90+
- First Contentful Paint: < 1.5s
- Time to Interactive: < 3s
- SEO Score: 100

## License

This project is for personal use. Feel free to use it as a template for your own portfolio.

## Credits

- Built with [Next.js](https://nextjs.org/)
- Animations by [Framer Motion](https://www.framer.com/motion/)
- Icons by [React Icons](https://react-icons.github.io/react-icons/)
- Design inspired by premium tech portfolios

---

**Built with ❤️ by Mathew Kioko | MathewTech**
