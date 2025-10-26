# ELCA Blockbusters - Frontend

**Next.js 16.0.0 frontend for ELCA AI ministry tools**

---

## Tech Stack

- **Framework:** Next.js 16.0.0 (Turbopack enabled)
- **React:** 19.2.0
- **UI Components:** Radix UI + shadcn/ui
- **Styling:** Tailwind CSS 3.4.18
- **State Management:** TanStack Query v5.90.5
- **Icons:** Lucide React 0.548.0
- **Forms:** React Hook Form + Zod validation
- **Animation:** Framer Motion 12.x

---

## Features

### 3 AI Agent Dashboards

1. **AI Pastor** - Sermon generation, devotionals, scripture studies
2. **Gen-Z Engine** - Social media content, youth engagement
3. **Miracle Finder** - Volunteer deployment, mission coordination

### ELCA Compliance
- ✅ ELCA 2025 AI Guidelines validated
- ✅ 8 core values integration
- ✅ 8 operational beliefs enforcement
- ✅ Bias detection and inclusive language
- ✅ Pastoral review requirements

---

## Quick Start

### Local Development

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Open browser
open http://localhost:3000
```

### Environment Variables

Create `.env.local`:
```env
NEXT_PUBLIC_API_URL=http://localhost:8000
```

For production:
```env
NEXT_PUBLIC_API_URL=https://elca-blockbusters-api.onrender.com
```

---

## Build Commands

```bash
# Development
npm run dev

# Production build
npm run build

# Start production server
npm start

# Lint code
npm run lint
```

---

## Backend Integration

This frontend connects to the FastAPI backend:
- **Local:** http://localhost:8000
- **Production:** https://elca-blockbusters-api.onrender.com
- **Backend Repo:** https://github.com/seanebones-lang/mothershipaddons

API client configuration in `lib/api-client.ts`

---

## Deployment

### Deploy to Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/seanebones-lang/eclathree)

**Manual deployment:**

1. Go to https://vercel.com
2. Import this repository
3. Framework: Next.js (auto-detected)
4. Root Directory: `.` (project root)
5. Add environment variable:
   - `NEXT_PUBLIC_API_URL=https://elca-blockbusters-api.onrender.com`
6. Click Deploy

**Production URL:** https://elca-blockbusters.vercel.app

---

## Project Structure

```
frontend/
├── app/
│   ├── page.tsx              # Main dashboard with 3 tabs
│   ├── layout.tsx            # Root layout with providers
│   ├── providers.tsx         # TanStack Query provider
│   ├── globals.css           # Tailwind + custom styles
│   ├── error.tsx             # Error boundary
│   └── api/                  # API routes (optional)
├── components/
│   ├── sermon_generator.tsx  # Pastoral Agent UI
│   ├── genz_dashboard.tsx    # Youth Engagement UI
│   ├── miracles_dashboard.tsx # Mission Coordination UI
│   └── ui/                   # shadcn/ui components
├── lib/
│   ├── api-client.ts         # Backend API integration
│   ├── schemas.ts            # Zod validation schemas
│   └── utils.ts              # Helper functions
├── hooks/
│   └── use-toast.ts          # Toast notifications
├── public/                   # Static assets
├── package.json              # Dependencies
├── tailwind.config.js        # Tailwind configuration
├── next.config.js            # Next.js configuration
├── vercel.json               # Vercel deployment config
└── tsconfig.json             # TypeScript configuration
```

---

## Key Dependencies

### UI Framework
- `next@16.0.0` - React framework with Turbopack
- `react@19.2.0` - UI library
- `react-dom@19.2.0` - React DOM renderer

### UI Components
- `@radix-ui/*` - Headless UI primitives
- `lucide-react@0.548.0` - Icon library
- `tailwindcss@3.4.18` - Utility-first CSS
- `framer-motion@12.23.24` - Animation library

### State & Data
- `@tanstack/react-query@5.90.5` - Async state management
- `react-hook-form@7.65.0` - Form management
- `zod@4.1.12` - Schema validation

### Content Rendering
- `react-markdown@10.1.0` - Markdown rendering
- `react-syntax-highlighter@16.0.0` - Code highlighting

---

## API Integration

The frontend communicates with the backend via REST API:

### Endpoints Used

**Agents:**
- `GET /api/agents` - List all AI agents
- `GET /api/agents/{id}` - Get specific agent

**Tasks:**
- `POST /api/tasks` - Create new AI task
- `GET /api/tasks/recent` - Get recent tasks

**Ontology:**
- `GET /api/ontology/values` - ELCA values
- `GET /api/ontology/beliefs` - ELCA beliefs
- `GET /api/ontology/summary` - Summary stats

**Health:**
- `GET /health` - Backend health check
- `GET /ready` - Readiness check

---

## Error Handling

- ✅ React error boundary (`app/error.tsx`)
- ✅ Try-catch blocks in all API calls
- ✅ Loading states for all queries
- ✅ Fallback UI for failed requests
- ✅ Toast notifications for user feedback

---

## Performance

- ✅ Turbopack for faster builds
- ✅ React 19 compiler optimizations
- ✅ Image optimization (Next.js)
- ✅ Code splitting (automatic)
- ✅ Global CDN (Vercel)
- ✅ Edge functions support

---

## ELCA 2025 AI Guidelines Compliance

All UI elements reflect ELCA values:
- **Radical Hospitality:** Inclusive language and welcoming tone
- **Grace-Centered Faith:** Positive, supportive messaging
- **Justice & Advocacy:** Accessibility and equity focus
- **Human Dignity:** Clear AI disclosure, pastoral review prompts

---

## Development

### Hot Reload
Changes to any `.tsx`, `.ts`, or `.css` file trigger automatic reload.

### Type Safety
Full TypeScript coverage with strict mode enabled.

### Linting
```bash
npm run lint
```

### Code Quality
- ESLint configured for Next.js
- TypeScript strict mode
- React 19 best practices

---

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

---

## License

See LICENSE file in main repository.

---

## Related Repositories

- **Backend API:** https://github.com/seanebones-lang/mothershipaddons
- **Documentation:** Included in backend repo

---

**Built for ELCA congregations with cutting-edge 2025 AI technology**

*AI should assist human ministry, not replace human discernment, especially in pastoral care, worship leadership, and spiritual guidance.* - ELCA 2025 AI Guidelines

