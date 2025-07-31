# Banking App Landing Page

A modern, responsive landing page for a multi-currency banking application built with Nuxt 3 and Tailwind CSS.

## Features

- **Responsive Design**: Mobile-first approach with seamless adaptation across all devices
- **Modern UI**: Clean, professional design with smooth animations and hover effects
- **Component-Based Architecture**: Modular Vue.js components for easy maintenance
- **Tailwind CSS**: Utility-first CSS framework for rapid styling
- **Nuxt 3**: Latest Vue.js framework with SSR capabilities

## Design Highlights

- Hero section with compelling messaging and phone mockup
- Feature showcase with send/receive money capabilities
- Trust indicators and partner logos
- Interactive sign-up form with validation
- Professional footer with organized links

## Tech Stack

- **Framework**: Nuxt 3
- **Styling**: Tailwind CSS
- **Language**: TypeScript/JavaScript
- **Package Manager**: npm

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm

### Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser

### Build for Production

```bash
npm run build
```

### Preview Production Build

```bash
npm run preview
```

## Project Structure

```
banking-app/
├── components/          # Vue components
│   ├── AppHeader.vue
│   ├── HeroSection.vue
│   ├── SendReceiveSection.vue
│   ├── FeaturesGrid.vue
│   ├── TrustedPartners.vue
│   ├── SignUpSection.vue
│   └── AppFooter.vue
├── pages/              # Page components
│   └── index.vue
├── assets/             # Static assets
│   └── css/
│       └── main.css
├── nuxt.config.ts      # Nuxt configuration
├── tailwind.config.js  # Tailwind configuration
└── package.json
```

## Components

### AppHeader
- Responsive navigation with mobile menu
- Logo and navigation links
- Call-to-action buttons

### HeroSection
- Main headline and value proposition
- Statistics display
- Phone mockup with realistic app interface
- Action buttons

### SendReceiveSection
- Feature descriptions for money transfer
- Two-column layout with icons and benefits

### FeaturesGrid
- Four key features in a responsive grid
- Icons and illustrations for each feature

### TrustedPartners
- Partner logos and trust indicators
- Security and compliance information

### SignUpSection
- Complete registration form
- Social login options
- Form validation and loading states

### AppFooter
- Company information and links
- Social media links
- Security indicators

## Customization

The design can be easily customized by modifying:

- **Colors**: Update the color palette in `tailwind.config.js`
- **Typography**: Modify font families and sizes in the Tailwind config
- **Content**: Update text content in individual components
- **Layout**: Adjust spacing and layout in component templates

## License

This project is for demonstration purposes.
