# 🛹 Suburbia Skateboards

A high-performance, visually immersive skateboard brand website featuring an **interactive 3D board customizer**, physics-based footer animations, GSAP scroll effects, and fully CMS-driven content — built with Next.js 15, React Three Fiber, GSAP, Matter.js, and Tailwind CSS.

---

## Table of Contents

- [🛹 Suburbia Skateboards](#-suburbia-skateboards)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
    - [3D \& Interactive](#3d--interactive)
    - [Animations \& Effects](#animations--effects)
    - [Content \& CMS Integration](#content--cms-integration)
    - [UI/UX \& Navigation](#uiux--navigation)
    - [Performance \& Developer Experience](#performance--developer-experience)
  - [Tech Stack](#tech-stack)
    - [Core Framework \& Runtime](#core-framework--runtime)
    - [3D \& Rendering](#3d--rendering)
    - [Animation \& Physics](#animation--physics)
    - [CMS \& Content](#cms--content)
    - [Styling](#styling)
    - [Utilities \& Tooling](#utilities--tooling)
  - [Deployment](#deployment)
    - [Live App](#live-app)
    - [Platform Details](#platform-details)
  - [How to Use App for Regular User](#how-to-use-app-for-regular-user)
    - [Browsing the Homepage](#browsing-the-homepage)
    - [Interactive Footer](#interactive-footer)
    - [Using the Board Customizer](#using-the-board-customizer)
  - [Getting Started (Developers)](#getting-started-developers)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
    - [Available Scripts](#available-scripts)
  - [Project Structure](#project-structure)
  - [CMS Integration (Prismic)](#cms-integration-prismic)
    - [Content Types](#content-types)
    - [Slice Machine](#slice-machine)
    - [API Routes](#api-routes)
  - [Environment Variables](#environment-variables)
    - [Environment Variable Reference](#environment-variable-reference)
    - [Notes](#notes)
  - [License](#license)

---

## Features

### 3D & Interactive

- ✅ **Interactive 3D Skateboard Viewer** — Full 3D skateboard model rendered with Three.js and React Three Fiber, featuring realistic PBR materials, HDR environment lighting, and real-time camera controls (orbit, pan, zoom)
- ✅ **Real-Time Board Customizer** — Live deck texture swapping, wheel customization, truck color selection, and bolt color selection on the `/build` page
- ✅ **Shareable Customizer State** — Board configurations are stored in URL search params (`?wheel=X&deck=Y&truck=Z&bolt=W`), making it easy to share a custom build with anyone
- ✅ **GLTF Model Loading** — Optimized 3D model loading with texture preloading for seamless transitions between component selections
- ✅ **Constant Wheel Spin Animation** — Featured hero skateboards display continuously spinning wheels for a dynamic visual effect
- ✅ **Advanced Material System** — Diffuse maps, normal maps, roughness maps, and specialized grip-tape bump mapping for photorealistic rendering

### Animations & Effects

- ✅ **GSAP-Powered Scroll Animations** — Scroll-triggered entrance animations throughout all content sections, with smooth camera transitions in the customizer
- ✅ **Parallax Mouse-Tracking Effect** — Foreground and background image layers on Text & Image sections that respond to mouse movement for depth
- ✅ **Intersection Observer Slide-In Reveals** — Content slides in from the side as it enters the viewport, with customizable delay and duration
- ✅ **SVG Squiggle Filter Animations** — Procedural noise-based distortion effects using feTurbulence with 5 animation frames and smooth hover transitions
- ✅ **Physics-Based Interactive Footer** — Skateboard decks fall with realistic gravity (Matter.js), supporting mouse drag interaction, responsive collision boundaries, reduced motion preferences, and mobile optimization

### Content & CMS Integration

- ✅ **Prismic CMS Content Management** — All page content is modular and managed through Prismic Slice Machine, enabling easy content updates without code changes
- ✅ **5 Dynamic Slice Types** — Hero (with 3D display), Product Grid (4-column), Team Grid (4-column), Text & Image (3 color themes), and Video Block (YouTube embed with custom masking)
- ✅ **Lazy-Loaded YouTube Player** — Video embeds load on demand for faster initial page loads
- ✅ **Dynamic Product Relationships** — Product Grid items link to individual skateboard content stored in Prismic
- ✅ **Board Customizer CMS Config** — Deck, wheel, truck, and bolt options are driven by Prismic content, making them easy to update
- ✅ **Draft Preview Mode** — Content editors can preview unpublished changes via authenticated preview endpoints

### UI/UX & Navigation

- ✅ **Responsive Header Navigation** — Logo, dynamic CMS-driven nav menu, and cart button with item count; adapts to mobile with a hamburger menu
- ✅ **Themed Button Components** — CTA buttons with icon support (skateboard, cart, plus) and multiple color variants (lime, orange, purple, blue)
- ✅ **Responsive Design** — Fluid typography and spacing via fluid-tailwind that scales seamlessly across all viewport sizes
- ✅ **Custom Brand Typography** — Bowlby One SC for display headings and DM Mono for body text, loaded via `next/font/google`
- ✅ **Custom Brand Color Palette** — Brand Blue, Lime, Navy, Orange, Pink, Purple, and Gray for a cohesive visual identity

### Performance & Developer Experience

- ✅ **Next.js 15 App Router** — Server Components, Turbopack dev server, and optimized routing
- ✅ **TypeScript** — Full type safety with auto-generated Prismic types
- ✅ **Optimized Image Handling** — `next/image` with Prismic image CDN and modern formats (WebP, AVIF)
- ✅ **Incremental Static Regeneration (ISR)** — Production caching with on-demand revalidation via webhooks
- ✅ **SEO & Metadata** — Automatic metadata generation from Prismic settings with OpenGraph image support

---

## Tech Stack

### Core Framework & Runtime

| Technology | Version | Purpose |
|---|---|---|
| **Next.js** | 15.5.12 | React framework with App Router & Turbopack |
| **React** | 19.2.3 | UI library |
| **TypeScript** | 5.x | Type safety |

### 3D & Rendering

| Technology | Version | Purpose |
|---|---|---|
| **Three.js** | 0.171.0 | 3D graphics engine |
| **React Three Fiber** | 9.0.0-rc.1 | React renderer for Three.js |
| **React Three Drei** | 9.120.4 | R3F utilities (controls, loaders, environment) |

### Animation & Physics

| Technology | Version | Purpose |
|---|---|---|
| **GSAP** | 3.12.5 | Advanced animation library |
| **@gsap/react** | 2.1.1 | GSAP React integration |
| **Matter.js** | 0.20.0 | 2D physics engine (footer interaction) |

### CMS & Content

| Technology | Version | Purpose |
|---|---|---|
| **@prismicio/client** | 7.13.0 | Prismic API client |
| **@prismicio/react** | 2.9.1 | Prismic React components |
| **@prismicio/next** | 1.7.1 | Prismic Next.js integration |

### Styling

| Technology | Version | Purpose |
|---|---|---|
| **Tailwind CSS** | 3.4.1 | Utility-first CSS framework |
| **fluid-tailwind** | 1.0.4 | Responsive fluid typography & spacing |
| **PostCSS** | 8.x | CSS processing |

### Utilities & Tooling

| Technology | Version | Purpose |
|---|---|---|
| **react-icons** | 5.4.0 | Icon library |
| **clsx** | 2.1.1 | Conditional className utility |
| **ESLint** | 8.x | Code linting |
| **Slice Machine UI** | 2.11.1 | Prismic content slice editor |

---

## Deployment

### Live App

**🔗 [https://suburbia-skate-next-gsap-3js-tcss-t.vercel.app](https://suburbia-skate-next-gsap-3js-tcss-t.vercel.app)**

### Platform Details

| Property | Value |
|---|---|
| **Platform** | Vercel |
| **Build Command** | `npm run build` |
| **Output** | Standalone Next.js build |
| **Node Version** | 18.x or higher |
| **CI/CD** | Automatic deployment on push to `main` |
| **Caching** | ISR with on-demand revalidation via Prismic webhooks |

---

## How to Use App for Regular User

### Browsing the Homepage

1. Open the app at [https://suburbia-skate-next-gsap-3js-tcss-t.vercel.app](https://suburbia-skate-next-gsap-3js-tcss-t.vercel.app).
2. Scroll down to enjoy animated sections — the hero section with an interactive 3D skateboard, featured products, team members, and video content.
3. Clicking Top, Middle, or Bottom sections of the  TOP part of the  3D interactive skateboard to see different types of movements of the 3D Skateboard.

### Interactive Footer

- At the bottom of the page, skateboard deck graphics fall using a real-time physics simulation.
- Click and drag them around — they bounce and collide realistically, powered by Matter.js.

### Using the Board Customizer

1. Click the **"Build Your Board"** button in the site header or navigate to `/build`.
2. Use the control panel to customize your board:
   - **Deck** — Browse and select from available deck designs.
   - **Wheels** — Choose a wheel style.
   - **Trucks** — Pick a truck color.
   - **Bolts** — Select a bolt color.
3. The 3D preview updates in real time as you make selections, with the camera smoothly transitioning to highlight the changed component.

---

## Getting Started (Developers)

### Prerequisites

- **Node.js** 18+ (20+ recommended)
- **npm** or **pnpm**
- **Git**

### Installation

```bash
# Clone the repository
git clone https://github.com/tauseefiqbal/suburbia_skate-next-gsap-3js-tcss-ts.git
cd suburbia_skate

# Install dependencies
npm install

# Start the development server (Turbopack)
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Available Scripts

| Script | Command | Description |
|---|---|---|
| `dev` | `npm run dev` | Start dev server with Turbopack |
| `build` | `npm run build` | Create production build |
| `start` | `npm run start` | Start production server |
| `lint` | `npm run lint` | Run ESLint |
| `slicemachine` | `npm run slicemachine` | Open Prismic Slice Machine editor |

---

## Project Structure

```
suburbia_skate/
├── public/                     # Static assets (textures, HDR maps)
│   ├── hdr/                    # HDR environment maps for 3D lighting
│   └── skateboard/             # Skateboard textures & normal maps
│
├── src/
│   ├── app/                    # Next.js App Router
│   │   ├── (with-header)/      # Routes with Header + Footer layout
│   │   │   ├── layout.tsx      # Header/Footer wrapper
│   │   │   └── page.tsx        # Homepage (Prismic SliceZone)
│   │   ├── build/              # Board customizer page
│   │   │   ├── context.tsx     # Customizer state management
│   │   │   ├── Controls.tsx    # Deck/Wheel/Truck/Bolt selectors
│   │   │   └── Preview.tsx     # 3D canvas (React Three Fiber)
│   │   ├── api/                # API routes (preview, revalidate)
│   │   └── slice-simulator/    # Slice Machine preview
│   │
│   ├── components/             # Reusable UI components
│   │   ├── Skateboard.tsx      # 3D skateboard model (R3F)
│   │   ├── FooterPhysics.tsx   # Matter.js physics footer
│   │   ├── Header.tsx          # Navigation header
│   │   ├── SlideIn.tsx         # Scroll animation wrapper
│   │   └── SVGFilters.tsx      # SVG squiggle filter effects
│   │
│   ├── slices/                 # Prismic slice components
│   │   ├── Hero/               # Hero section with 3D skateboard
│   │   ├── ProductGrid/        # Product showcase grid
│   │   ├── TeamGrid/           # Team member grid
│   │   ├── TextAndImage/       # Content section with parallax
│   │   └── VideoBlock/         # Lazy YouTube embed
│   │
│   └── lib/                    # Utility hooks
│
├── customtypes/                # Prismic content type schemas
└── slicemachine.config.json    # Slice Machine configuration
```

---

## CMS Integration (Prismic)

### Content Types

| Type | Description |
|---|---|
| `homepage` | Main landing page composed of dynamic slices |
| `settings` | Site-wide settings (navigation links, footer images, metadata) |
| `skateboard` | Individual skateboard product data |
| `skater` | Team member / skater profiles |
| `board_customizer` | Customizer options (decks, wheels, trucks, bolts) |

### Slice Machine

Run the Slice Machine editor locally to manage content slices:

```bash
npm run slicemachine
```

The slice simulator is available at [http://localhost:3000/slice-simulator](http://localhost:3000/slice-simulator) for previewing slices during development.

**Available Slices:**

| Slice | Description |
|---|---|
| `Hero` | Full-screen hero with heading, CTA, and interactive 3D skateboard |
| `ProductGrid` | 4-column product grid with images, names, and prices |
| `TeamGrid` | 4-column team member grid with photos and bios |
| `TextAndImage` | Two-column section with text, CTA, and parallax image (3 color themes) |
| `VideoBlock` | YouTube video embed with custom SVG masking |

### API Routes

| Route | Method | Purpose |
|---|---|---|
| `/api/preview` | `GET` | Enter Prismic draft preview mode |
| `/api/exit-preview` | `GET` | Exit preview mode and return to live content |
| `/api/revalidate` | `POST` | Trigger on-demand ISR cache revalidation via webhook |

---

## Environment Variables

This project uses environment variables to configure the Prismic CMS connection. For local development, create a `.env.local` file in the root directory:

```bash
# .env.local (create this file for local development)
NEXT_PUBLIC_PRISMIC_ENVIRONMENT=suburbia
```

### Environment Variable Reference

| Variable | Required | Default | Description |
|---|---|---|---|
| `NEXT_PUBLIC_PRISMIC_ENVIRONMENT` | No | `suburbia` | Prismic repository name (defined in `slicemachine.config.json`) |
| `NODE_ENV` | Auto-set | `development` | Node environment (`development` or `production`) — automatically set by Next.js |

### Notes

- **`NEXT_PUBLIC_*` variables** are exposed to the browser and can be used in client-side code.
- The `NEXT_PUBLIC_PRISMIC_ENVIRONMENT` variable is optional because it defaults to the `repositoryName` value from `slicemachine.config.json`.
- **For production deployment on Vercel**, environment variables are configured in the Vercel dashboard and automatically injected during build time.

---

## License

This project is licensed under the MIT License.
