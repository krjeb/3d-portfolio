# Kristofer — 3D Web Developer Portfolio

An interactive 3D developer portfolio built with React 19, Three.js, GSAP, and Tailwind CSS.

## Tech Stack

- **Frontend / Framework:** React 19, Vite, Tailwind CSS v4, TypeScript
- **3D & Animation:** Three.js, React Three Fiber, React Three Drei, React Three Postprocessing, GSAP
- **Integrations & Services:** EmailJS (Contact API), React CountUp

## Acknowledgements & Credits

- **Original Project Tutorial:** Built following the 3D Web Developer Portfolio course by [JavaScript Mastery](https://www.youtube.com/@javascriptmastery) ([Watch on YouTube](https://youtu.be/0fYi8SGA20k?si=XBjzV8utEcppSXLb)).

## Key Improvements & Refactoring (Beyond the Tutorial)

### 1. Module Resolution & Build Stability

- **Export & Import Normalization:** Fixed default/named export mismatches across component modules (`LogoSection`, `Footer`, `ExperienceSection`, `TechIcon`) that caused white-screen runtime crashes.
- **CJS/ESM Interop Resolution:** Resolved Vite/Rolldown default-export interop issues with `CountUp` to ensure stable SSR and CSR component hydration.
- **Animation Plugin Registration:** Corrected `ScrollTrigger` module casing and scope registration to restore scroll-driven GSAP timeline sequences.

### 2. Canvas Layout & Rendering Optimization

- **3D Scene Alignment:** Recalibrated `HeroExperience` viewport coordinates and canvas boundaries for precise spatial alignment with 2D DOM text elements.
- **Reconciliation & Key Stability:** Re-indexed collection mappings across interactive 3D elements to resolve duplicate key warnings and optimize React reconciliation.
