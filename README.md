# Voz.IA - AI Voice Application

This is a Next.js application with Vercel Speed Insights integrated for performance monitoring.

## Features

- **Vercel Speed Insights**: Real-time performance monitoring integrated via `@vercel/speed-insights` package
- **Next.js 14+**: Modern React framework for production
- **TypeScript**: Type-safe development
- **Tailwind CSS**: Utility-first CSS framework

## Getting Started

### Prerequisites

- Node.js 18+ installed
- A Vercel account (for deploying and viewing Speed Insights data)

### Installation

1. Install dependencies:
```bash
npm install
# or
pnpm install
# or
yarn install
# or
bun install
```

2. Run the development server:
```bash
npm run dev
# or
pnpm dev
# or
yarn dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## Vercel Speed Insights Integration

This project includes Vercel Speed Insights for monitoring Core Web Vitals and other performance metrics.

### Setup Steps Completed

1. **Package Installation**: The `@vercel/speed-insights` package has been added to `package.json`

2. **Component Integration**: The `<SpeedInsights />` component from `@vercel/speed-insights/next` has been integrated in the root layout:
   - Location: `app/layout.tsx`
   - The component automatically collects Web Vitals and sends them to Vercel

3. **Next.js App Router**: Uses the modern App Router structure (Next.js 13+)

### Enabling Speed Insights in Vercel Dashboard

To view your Speed Insights data:

1. Go to [Vercel Dashboard](https://vercel.com/dashboard)
2. Select your project
3. Navigate to the **Speed Insights** tab
4. Click **Enable** (if not already enabled)
5. Deploy your project to Vercel
6. Wait for users to visit your site to start collecting metrics

### Deploying to Vercel

```bash
# Using Vercel CLI
npm i -g vercel
vercel deploy

# Or connect your Git repository to Vercel for automatic deployments
```

After deployment, the Speed Insights script will be automatically available at `/_vercel/speed-insights/script.js`

## Performance Metrics

Vercel Speed Insights tracks:
- **LCP** (Largest Contentful Paint)
- **FID** (First Input Delay) / INP (Interaction to Next Paint)
- **CLS** (Cumulative Layout Shift)
- **DNS** and **TCP** connection times
- **TTFB** (Time to First Byte)

## Project Structure

```
├── app/
│   ├── layout.tsx          # Root layout with SpeedInsights component
│   ├── page.tsx            # Home page
│   └── globals.css         # Global styles
├── package.json            # Dependencies including @vercel/speed-insights
├── tsconfig.json           # TypeScript configuration
├── tailwind.config.ts      # Tailwind CSS configuration
├── postcss.config.js       # PostCSS configuration
└── next.config.js          # Next.js configuration
```

## Building for Production

```bash
npm run build
npm start
```

## Linting

```bash
npm run lint
```

## Further Reading

- [Vercel Speed Insights Documentation](https://vercel.com/docs/speed-insights)
- [Next.js Documentation](https://nextjs.org/docs)
- [Web Vitals](https://web.dev/vitals/)

## License

MIT
