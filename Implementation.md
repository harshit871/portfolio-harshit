# Harshit Soni - Portfolio Implementation Plan

This document outlines the step-by-step technical plan to develop your modern, performant, and SEO-optimized portfolio utilizing Next.js (App Router), Tailwind CSS, TypeScript, and Shadcn UI, according to the details extracted from your resume.

## User Review Required

> [!IMPORTANT]
> Please review the chosen tech stack and the planned sections. Let me know if you have specific projects (with names, descriptions, and links) you'd like me to feature in the "Projects" section, as your resume primarily details enterprise projects under your professional experience. I will use realistic placeholders for personal projects if none are provided.
> 
> Additionally, let me know if you would like me to use a specific generic backend for your contact form (like Formspree or EmailJS) or just implement a `mailto` link for now.

## Proposed Setup and Implementation

### 1. Project Initialization & Tooling
- Initialize a new Next.js 15 project (App Router, TypeScript, Tailwind CSS, ESLint).
- Configure `next-themes` to support smooth Light/Dark mode toggling.
- Setup `shadcn/ui` to quickly scaffold accessible and beautiful components.
- Install Lucide React for consistent SVG icons.
- Configure highly-optimized fonts (e.g., `Inter` and a sleek serif or mono for accents).

### 2. Architecture & File Structure
Following the Next.js App Router paradigm, I will structure the source code:
- `app/layout.tsx`: Main layout, global SEO metadata, theme provider, and global Navbar/Footer.
- `app/page.tsx`: A single-page scroll layout containing all portfolio sections.
- `components/ui/*`: Shadcn basic elements (Buttons, Cards, Badges).
- `components/sections/*`: Dedicated components for Hero, About, Experience, Skills, Projects, Achievements, and Contact.
- `lib/data.ts`: A centralized file housing your resume data (Experience, Education, Skills, etc.) so you can easily update it later.

### 3. Section Implementations

* **Header/Navbar**: Fixed transparent-to-opaque blur header. Includes navigation links and a Dark Mode toggle.
* **Hero Section**: Strong introductory typography, role ("Front-end Developer"), a brief punchy summary, CTA buttons ("Hire Me", "View Resume"), and subtle background gradients/animations.
* **About Section**: Highlighting your 4 years of experience and focus on high-performance product building.
* **Experience Timeline**: A vertical timeline component showcasing roles at Aerem Solutions, Fluent Health, and Cogoport, with metrics-driven bullet points (e.g., SEO score 92, 15% boost).
* **Skills/Tech Stack**: A grid featuring modern badges for languages and tools (React, Next.js, Tailwind, TypeScript, etc.).
* **Projects**: 3-6 interactive cards with hover effects featuring images/placeholders, technical stack badges, and GitHub/Demo links.
* **Achievements & Education**: Clean list/cards for your First Division Honors, Top 1% NPTEL, HackerRank certification, etc.
* **Contact Section**: A simple, aesthetic form UI and your social links (LinkedIn, GitHub).

### 4. Design Direction
- **Vibe**: Sleek, modern, minimalist, dynamic.
- **Color Palette**: Dark mode by default (tailored zinc/slate colors), subtle primary brand color (e.g., a vibrant indigo or teal) for buttons and link hovers.
- **Micro-interactions**: Hover lifts on cards, faded intersections on scroll (using Framer Motion or Tailwind animate), sleek transitions on color theme change.

### 5. SEO & Performance Optimization
- Native Next.js server-side static rendering (SSG where possible).
- `next/image` for automatic image optimization.
- Semantic HTML tags (`<section>`, `<article>`, `<nav>`).
- Dynamic Metadata for rich sharing previews (Open Graph labels).

## Open Questions

> [!WARNING]  
> - Are there any specific personal projects (Title, Description, Tech Stack, URLs) you want me to include? 
> - For the resume download, do you plan to host the PDF in the `public` folder? I can set up the download link to assume `/harshit-soni-resume.pdf`.

## Verification Plan

### Automated/Tool Verification
- Run a Lighthouse check locally to verify performance, accessibility, SEO, and best practices scores are > 90.
- Verify production build finishes without warnings (`npm run build`).

### Manual Verification
- Test responsiveness across mobile, tablet, and desktop viewports.
- Click all internal soft-scroll links and test the dark mode toggle.
- Visually QA the gradients and animations.
