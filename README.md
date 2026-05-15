# FunnelForge – Professional Drag-and-Drop Funnel Builder

## What is FunnelForge?

FunnelForge is a modern SaaS platform that lets you build high-converting sales funnels in minutes, without any coding required. Inspired by ClickFunnels but optimized for speed and simplicity.

### Key Features

✨ **Drag-and-Drop Editor** — Intuitive step builder with multiple template types (Landing, Opt-In, Sales, Upsell, Thank You)

🔍 **Live Preview** — See your changes in real-time as you edit

🎨 **Full Customization** — Control colors, fonts, copy, CTAs, and layout for every step

💾 **Save & Export** — Export funnels as JSON or HTML for deployment

📱 **Mobile-Responsive** — All funnels render perfectly on mobile and desktop

🔄 **Reorder Steps** — Drag steps to reorder your funnel flow

## Getting Started

### Installation

```bash
git clone https://github.com/Goatkenziee/funnel-forge.git
cd funnel-forge
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Usage

1. **Create a Funnel** — Click "New Funnel" from the dashboard
2. **Add Steps** — Use the sidebar to add Landing, Opt-In, Sales, Upsell, or Thank You pages
3. **Customize** — Edit headlines, copy, colors, and CTA buttons in the right panel
4. **Preview** — Toggle preview mode to see how your funnel looks
5. **Export** — Export as JSON to backup or import elsewhere

## Architecture

- **Frontend**: Next.js 14 (App Router) + React + TypeScript
- **Styling**: Tailwind CSS
- **State Management**: Zustand
- **Icons**: Lucide React
- **Storage**: Browser LocalStorage (persistent across sessions)

## Project Structure

```
funnel-forge/
├── app/
│   ├── page.tsx              # Landing page
│   ├── layout.tsx            # Root layout
│   ├── globals.css           # Global styles
│   ├── dashboard/
│   │   └── page.tsx          # Funnel management dashboard
│   └── editor/
│       └── [id]/
│           └── page.tsx      # Drag-drop funnel editor
├── components/
│   ├── Sidebar.tsx           # Step list & templates
│   ├── StepEditor.tsx        # Edit panel for step config
│   └── StepPreview.tsx       # Live preview of step
├── lib/
│   ├── store.ts              # Zustand state management
│   ├── types.ts              # TypeScript interfaces
│   └── utils.ts              # Helper functions
├── package.json
└── README.md
```

## How It Works

### State Management (Zustand)

The app uses Zustand to manage all funnel data:
- Create/update/delete funnels
- Add/edit/remove steps
- Persist to LocalStorage automatically
- Export/import funnel JSON

### Step Types

- **Landing** — Hero section with headline, subheadline, and CTA
- **Opt-In** — Email capture form with benefits
- **Sales** — Product showcase with pricing and features
- **Upsell** — Additional offer after purchase
- **Thank You** — Confirmation and next steps
- **Custom** — Blank template for any use case

### Preview Mode

Toggle between:
- **Edit Mode** — Full editor with live preview on the left, settings on the right
- **Preview Mode** — Full-screen preview of your step

## Deployment

### Deploy to Vercel (Recommended)

```bash
npm install -g vercel
vercel
```

Your app will be live in ~30 seconds.

### Deploy Anywhere

FunnelForge works on any Node.js hosting:

```bash
npm run build
npm start
```

## Roadmap

- [ ] User authentication & accounts
- [ ] Database integration (Supabase/Firebase)
- [ ] Team collaboration
- [ ] Advanced analytics & conversion tracking
- [ ] Template library with pre-designed funnels
- [ ] Email integration (Mailchimp, ConvertKit)
- [ ] Payment processing (Stripe integration)
- [ ] Custom domain hosting
- [ ] A/B testing

## License

MIT

## Support

Questions? Open an issue or start a discussion on GitHub.
