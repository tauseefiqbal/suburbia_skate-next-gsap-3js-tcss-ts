# 🛹 Suburbia Skateboards

A high-performance, visually immersive skateboard brand website featuring interactive 3D skateboard models, a real-time board customizer, physics-based animations, and CMS-driven content — built with Next.js 15, Three.js, GSAP, and Prismic.

![Next.js](https://img.shields.io/badge/Next.js-15-black?logo=next.js)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react)
![Three.js](https://img.shields.io/badge/Three.js-0.171-black?logo=three.js)
![GSAP](https://img.shields.io/badge/GSAP-3.12-88CE02)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-06B6D4?logo=tailwindcss)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript)

---

## 📑 Table of Contents

- [🛹 Suburbia Skateboards](#-suburbia-skateboards)
  - [📑 Table of Contents](#-table-of-contents)
  - [✅ Features](#-features)
    - [3D \& Interactive](#3d--interactive)
    - [Animations \& Effects](#animations--effects)
    - [Content \& CMS](#content--cms)
    - [Performance \& DX](#performance--dx)
  - [🛠 Tech Stack](#-tech-stack)
    - [Core Framework](#core-framework)
    - [3D \& Rendering](#3d--rendering)
    - [Animation](#animation)
    - [Styling](#styling)
    - [CMS \& Content](#cms--content)
    - [Physics](#physics)
    - [Utilities](#utilities)
  - [🚀 Deployment](#-deployment)
  - [🧑‍💻 How to Use App for Regular User](#-how-to-use-app-for-regular-user)
    - [Browsing the Homepage](#browsing-the-homepage)
    - [Customizing a Skateboard](#customizing-a-skateboard)
    - [Exploring Products \& Team](#exploring-products--team)
    - [Watching Videos](#watching-videos)
    - [Interactive Footer](#interactive-footer)
  - [🧰 Getting Started (Developers)](#-getting-started-developers)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
    - [Development](#development)
    - [Build for Production](#build-for-production)
    - [Prismic Slice Machine](#prismic-slice-machine)
  - [📁 Project Structure](#-project-structure)
  - [🔑 Environment Variables](#-environment-variables)
  - [📄 License](#-license)

---

## ✅ Features

### 3D & Interactive

- ✅ Interactive 3D skateboard model rendered with Three.js and React Three Fiber
- ✅ Real-time board customizer — swap decks, wheels, trucks, and bolts live in 3D
- ✅ Shareable customizer state via URL search params
- ✅ GLTF model loading with texture preloading for seamless transitions
- ✅ HDR environment lighting for realistic skateboard rendering
- ✅ Constant wheel spin animation on featured boards

### Animations & Effects

- ✅ GSAP-powered scroll and entrance animations throughout the site
- ✅ Parallax mouse-tracking image effect on Text & Image sections
- ✅ Intersection Observer–based slide-in reveal animations
- ✅ SVG squiggle filter animations with custom CSS keyframes
- ✅ Physics-based interactive footer using Matter.js — skateboard decks fall and respond to mouse drag

### Content & CMS

- ✅ Prismic CMS integration with Slice Machine for modular, editable page sections
- ✅ Dynamic slices: Hero, Product Grid, Team Grid, Text & Image, Video Block
- ✅ Lazy-loaded YouTube video player embedded via Video Block slice
- ✅ Team member grid dynamically populated from Prismic content
- ✅ Product grid with linked skateboard content relationships
- ✅ SEO metadata and Open Graph images managed via Prismic Settings

### Performance & DX

- ✅ Next.js 15 App Router with server components and Turbopack dev server
- ✅ Fully typed with TypeScript — auto-generated Prismic types
- ✅ Fluid responsive typography and spacing via `fluid-tailwind`
- ✅ Optimized image handling with `next/image` and Prismic image CDN
- ✅ Preview and exit-preview API routes for Prismic draft content
- ✅ Custom Google Fonts (Bowlby One SC, DM Mono) loaded via `next/font`

---

## 🛠 Tech Stack


### Core Framework

| Technology | Version | Purpose |
|---|---|---|
| **Next.js** | 15 | React framework with App Router, server components, Turbopack |
| **React** | 19 | UI library |
| **TypeScript** | 5 | Type safety |

### 3D & Rendering

| Technology | Version | Purpose |
|---|---|---|
| **Three.js** | 0.171 | 3D graphics engine |
| **React Three Fiber** | 9 (RC) | Declarative Three.js for React |
| **React Three Drei** | 9.120 | Helpers — `useGLTF`, `useTexture`, environment maps |

### Animation

| Technology | Version | Purpose |
|---|---|---|
| **GSAP** | 3.12 | High-performance scroll and entrance animations |
| **@gsap/react** | 2.1 | React integration for GSAP |

### Styling

| Technology | Version | Purpose |
|---|---|---|
| **Tailwind CSS** | 3.4 | Utility-first CSS framework |
| **fluid-tailwind** | 1.0 | Fluid responsive typography and spacing |
| **clsx** | 2.1 | Conditional class name joining |

### CMS & Content

| Technology | Version | Purpose |
|---|---|---|
| **Prismic** | 7.13 | Headless CMS for pages, products, team, settings |
| **Slice Machine** | 2.11 | Visual slice editor and code scaffolding |
| **@prismicio/next** | 1.7 | Next.js integration (images, links, previews) |

### Physics

| Technology | Version | Purpose |
|---|---|---|
| **Matter.js** | 0.20 | 2D physics engine for interactive footer |

### Utilities

| Technology | Purpose |
|---|---|
| **react-icons** | Icon library |
| **PostCSS** | CSS processing pipeline |
| **ESLint** | Code linting |

---

## 🚀 Deployment

The app is live and deployed on **Vercel**.

🔗 **Live URL:** [https://suburbia-skate-next-gsap-3js-tcss-t.vercel.app/](https://suburbia-skate-next-gsap-3js-tcss-t.vercel.app/)

---

## 🧑‍💻 How to Use App for Regular User

No installation or account is needed — simply visit the live site and explore.

### Browsing the Homepage

1. Open the [live site](https://suburbia-skate-next-gsap-3js-tcss-t.vercel.app/) in any modern browser.
2. Scroll down to enjoy animated sections — the hero banner features a rotating 3D skateboard, and content slides into view as you scroll.

### Customizing a Skateboard

1. Click the **"Build Your Board"** button in the site header.
2. The 3D Board Customizer opens with a live skateboard model.
3. Use the on-screen controls to swap out:
   - **Deck** — choose from different deck graphic and color options.
   - **Wheels** — pick a wheel color/style.
   - **Trucks** — select a truck metal finish.
   - **Bolts** — choose a bolt metal finish.
4. The 3D model updates in real time as you make selections.

### Exploring Products & Team

- **Product Grid** — browse the featured skateboard lineup with images and links.
- **Team Grid** — meet the skaters featured on the team, with profile images and scribble-style decorations.

### Watching Videos

- Scroll to the video section and click play — the YouTube player loads lazily to keep the page fast.

### Interactive Footer

- At the bottom of the page, skateboard deck graphics fall using physics simulation.
- Click and drag them around — they bounce and collide realistically powered by Matter.js.

---

## 🧰 Getting Started (Developers)

### Prerequisites

- **Node.js** 18+ installed
- **npm** or **yarn** package manager
- A [Prismic](https://prismic.io/) account with a repository named `suburbia`

### Installation

```bash
# Clone the repository
git clone https://github.com/tauseefiqbal/suburbia_skate-next-gsap-3js-tcss-ts.git

# Navigate into the project directory
cd suburbia_skate-next-gsap-3js-tcss-ts

# Install dependencies
npm install
```

### Development

```bash
# Start the development server with Turbopack
npm run dev
```

The app will be available at [http://localhost:3000](http://localhost:3000).

### Build for Production

```bash
# Create an optimized production build
npm run build

# Start the production server
npm start
```

### Prismic Slice Machine

```bash
# Launch the Slice Machine UI to manage content models
npm run slicemachine
```

The Slice Machine UI will open at [http://localhost:9999](http://localhost:9999), and the local slice simulator is available at [http://localhost:3000/slice-simulator](http://localhost:3000/slice-simulator).

---

## 📁 Project Structure

```
suburbia_skate/
├── public/                     # Static assets (textures, HDR maps)
│   ├── hdr/                    # HDR environment maps for 3D lighting
│   └── skateboard/             # Skateboard model textures
├── src/
│   ├── app/
│   │   ├── (with-header)/      # Route group with header layout
│   │   ├── api/                # API routes (preview, revalidate)
│   │   ├── build/              # Board customizer page
│   │   └── fonts/              # Font files
│   ├── components/             # Shared UI components
│   │   ├── Skateboard.tsx      # 3D skateboard model (Three.js)
│   │   ├── FooterPhysics.tsx   # Matter.js physics footer
│   │   ├── Header.tsx          # Site navigation header
│   │   ├── Footer.tsx          # Site footer
│   │   └── SlideIn.tsx         # Scroll-triggered reveal animation
│   ├── lib/                    # Utility hooks
│   └── slices/                 # Prismic slice components
│       ├── Hero/               # Hero section with interactive 3D board
│       ├── ProductGrid/        # Product showcase grid
│       ├── TeamGrid/           # Team members grid
│       ├── TextAndImage/       # Parallax text & image section
│       └── VideoBlock/         # Lazy-loaded YouTube embed
├── customtypes/                # Prismic custom type definitions
└── slicemachine.config.json    # Slice Machine configuration
```

---

## 🔑 Environment Variables

Create a `.env.local` file in the project root with your Prismic repository credentials:

```env
NEXT_PUBLIC_PRISMIC_ENVIRONMENT=your-prismic-repo-name
```

---

## 📄 License

This project is for educational and portfolio purposes.
