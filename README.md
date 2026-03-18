# Suburbia Skateboards

A skateboard shop website built with **Next.js 15**, **Prismic CMS**, **Three.js**, and **GSAP** animations.

## Tech Stack

- **Framework:** [Next.js 15](https://nextjs.org/) (Turbopack)
- **CMS:** [Prismic](https://prismic.io/) with Slice Machine
- **3D:** [React Three Fiber](https://docs.pmnd.rs/react-three-fiber) / [Three.js](https://threejs.org/)
- **Animation:** [GSAP](https://gsap.com/)
- **Physics:** [Matter.js](https://brm.io/matter-js/)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/)
- **Language:** TypeScript

## Getting Started

### Prerequisites

- Node.js 18+
- npm

### Installation

```bash
npm install
```

### Development

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Slice Machine

To manage Prismic slices and content models:

```bash
npm run slicemachine
```

### Production Build

```bash
npm run build
npm start
```

## Project Structure

```
src/
├── app/              # Next.js App Router pages & layouts
│   ├── build/        # Board customizer page
│   └── api/          # API routes (preview, revalidation)
├── components/       # Shared UI components (Header, Footer, Skateboard, etc.)
├── slices/           # Prismic slices
│   ├── Hero/         # Hero section with interactive skateboard
│   ├── ProductGrid/  # Product grid display
│   ├── TeamGrid/     # Team members grid
│   ├── TextAndImage/ # Text and image with parallax
│   └── VideoBlock/   # YouTube video embed
└── lib/              # Utility hooks
public/
├── hdr/              # HDR environment maps for 3D rendering
└── skateboard/       # Skateboard texture assets
```

## Scripts

| Command              | Description                        |
| -------------------- | ---------------------------------- |
| `npm run dev`        | Start dev server with Turbopack    |
| `npm run build`      | Create production build            |
| `npm start`          | Start production server            |
| `npm run lint`       | Run ESLint                         |
| `npm run slicemachine` | Launch Prismic Slice Machine UI  |
