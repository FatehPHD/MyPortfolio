# Fateh Ali Bukhari - Portfolio Website

A modern, responsive portfolio website showcasing projects, skills, experience, and education. Built with React and featuring a beautiful dark mode theme.

## ✨ Features

- 🎨 Modern, clean UI with smooth animations and transitions
- 🌙 Dark mode support with system preference detection
- 📱 Fully responsive design (mobile, tablet, desktop)
- 🚀 Built with React 18 and Vite for fast development
- 💅 Styled with Tailwind CSS with custom color palette
- 🎯 Smooth scrolling navigation with active section highlighting
- 📄 Dynamic project detail pages with React Router
- 📹 Video placeholders for projects (ready for your videos)
- 📧 Contact section with email and phone integration
- 📄 Resume download functionality
- 🎓 Education and experience sections
- 💼 Featured projects showcase

## 🛠️ Technologies Used

- **React 18** - UI library
- **Vite** - Build tool and dev server
- **React Router DOM** - Client-side routing
- **Tailwind CSS** - Utility-first CSS framework
- **React Icons** - Icon library
- **PostCSS** - CSS processing

## 📁 Project Structure

```
MyPortfolio/
├── public/
│   ├── profile.jpg          # Profile photo
│   ├── resume/              # Resume PDF files
│   └── videos/              # Project video files
├── src/
│   ├── components/          # Reusable components
│   │   ├── About.jsx
│   │   ├── Contact.jsx
│   │   ├── Education.jsx
│   │   ├── Experience.jsx
│   │   ├── Footer.jsx
│   │   ├── Header.jsx
│   │   ├── Projects.jsx
│   │   └── Skills.jsx
│   ├── contexts/
│   │   └── ThemeContext.jsx # Dark mode theme context
│   ├── data/
│   │   └── projects.js      # Project data
│   ├── pages/
│   │   ├── Home.jsx         # Main landing page
│   │   └── ProjectDetail.jsx # Individual project pages
│   ├── App.jsx              # Main app component with routing
│   ├── main.jsx             # Entry point
│   └── index.css            # Global styles
├── netlify.toml             # Netlify deployment config
├── vercel.json              # Vercel deployment config
└── package.json             # Dependencies and scripts
```

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v16 or higher recommended)
- **npm** or **yarn** package manager

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd MyPortfolio
```

   Or if you already have the repository:
```bash
cd MyPortfolio
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:5173`

The development server will automatically reload when you make changes to the code.

### Building for Production

To create an optimized production build:

```bash
npm run build
```

The built files will be in the `dist` directory, ready for deployment.

To preview the production build locally:

```bash
npm run preview
```

## 📹 Adding Project Videos

To add videos to your projects:

1. Place your video files in the `public/videos/` directory
2. Name them according to the project ID (e.g., `study-planner.mp4`, `subway-screen.mp4`)
3. The videos will automatically be displayed in the project detail pages

Note: Currently, the portfolio uses placeholder video elements. To enable video playback, update the `ProjectDetail.jsx` component to include video elements:

```jsx
<video className="w-full h-full object-cover rounded" controls>
  <source src={`/videos/${project.id}.mp4`} type="video/mp4" />
  Your browser does not support the video tag.
</video>
```

## 🌐 Deployment

This portfolio is configured for deployment on both **Netlify** and **Vercel**. Both platforms support single-page applications (SPAs) with client-side routing.

### Option 1: Deploy to Netlify

1. **Via Netlify CLI:**
   ```bash
   # Install Netlify CLI globally (if not already installed)
   npm install -g netlify-cli
   
   # Login to Netlify
   netlify login
   
   # Deploy
   npm run build
   netlify deploy --prod
   ```

2. **Via Netlify Dashboard:**
   - Push your code to GitHub/GitLab/Bitbucket
   - Go to [Netlify](https://www.netlify.com/)
   - Click "New site from Git"
   - Connect your repository
   - Build settings:
     - **Build command:** `npm run build`
     - **Publish directory:** `dist`
   - Click "Deploy site"

The `netlify.toml` file is already configured with the correct build settings and SPA redirect rules.

### Option 2: Deploy to Vercel

1. **Via Vercel CLI:**
   ```bash
   # Install Vercel CLI globally (if not already installed)
   npm install -g vercel
   
   # Login to Vercel
   vercel login
   
   # Deploy
   vercel --prod
   ```

2. **Via Vercel Dashboard:**
   - Push your code to GitHub/GitLab/Bitbucket
   - Go to [Vercel](https://vercel.com/)
   - Click "New Project"
   - Import your repository
   - Build settings:
     - **Framework Preset:** Vite
     - **Build Command:** `npm run build`
     - **Output Directory:** `dist`
   - Click "Deploy"

The `vercel.json` file is already configured with the correct SPA rewrite rules.

### Option 3: Deploy to GitHub Pages

1. Install `gh-pages` package:
   ```bash
   npm install --save-dev gh-pages
   ```

2. Add to `package.json` scripts:
   ```json
   "scripts": {
     "predeploy": "npm run build",
     "deploy": "gh-pages -d dist"
   }
   ```

3. Update `vite.config.js`:
   ```js
   export default defineConfig({
     plugins: [react()],
     base: '/MyPortfolio/' // Replace with your repo name
   })
   ```

4. Deploy:
   ```bash
   npm run deploy
   ```

## 📝 Customization

### Updating Personal Information

- **Profile Photo:** Replace `public/profile.jpg` with your own photo
- **Resume:** Replace `public/resume/Fateh_Ali_Bukhari_Resume.pdf` with your resume PDF
- **Contact Info:** Update email, phone, and social links in `src/components/About.jsx`
- **Projects:** Edit project data in `src/data/projects.js`
- **Skills:** Update skills list in `src/components/Skills.jsx`
- **Experience:** Update work experience in `src/components/Experience.jsx`
- **Education:** Update education details in `src/components/Education.jsx`

### Theme Customization

The theme uses custom Tailwind colors defined in `tailwind.config.js`. You can modify the color palette to match your preferences.

## 📄 License

This project is open source and available under the MIT License.

---

## 🙏 Acknowledgments

Built with passion and attention to detail. Thank you for visiting!

## 👤 Author

**Fateh Ali Bukhari**

- LinkedIn: [fatehalibukhari](https://www.linkedin.com/in/fatehalibukhari/)
- GitHub: [FatehPHD](https://github.com/FatehPHD)
- Email: ShahjiFateh@gmail.com
- Phone: (587) 664-1333

