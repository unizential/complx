<div align="center">
  <img src="branding/logo.svg" alt="Complexity Logo" width="120" height="120" />
</div>

<div align="center">

# Complexity

⚡ Supercharge your favourite AI Chat web apps

<div>💖 support the development</div>
<a href="https://paypal.me/pnd280" target="_blank"><img src="https://img.shields.io/badge/Paypal-blue?logo=paypal&logoColor=white" alt="Paypal"></a>
<a href="https://ko-fi.com/pnd280" target="_blank"><img src="https://img.shields.io/badge/Ko--fi-orange?logo=kofi&logoColor=white" alt="Ko-fi"></a>

<div>
  <a href="https://discord.cplx.app" target="_blank"><img src="https://img.shields.io/discord/1245377426331144304?logo=discord&label=discord&link=https%3A%2F%2Fdiscord.gg%2FfxzqdkwmWx" alt="Discord"></a>
</div>

</div>

> [!NOTE]
> Originally a [Perplexity AI](https://perplexity.ai/) extension, this repository has now been restructured into a suite of enhancements for multiple platforms and services.

## 🎨 **NEW: Complete Artifact Rendering System**

The Complexity extension now includes a comprehensive **Artifact Rendering System** that transforms it into a powerful creative coding and visualization platform. This system supports:

### **Supported Artifact Types:**
- ✨ **p5.js Creative Coding** - Generative art and interactive sketches
- 🎲 **Three.js 3D Graphics** - 3D scenes with physics
- 📊 **D3.js Data Visualization** - Charts and data exploration  
- ⚛️ **React Components** - Interactive UI components
- 🌐 **HTML Pages** - Complete web applications
- 🎨 **SVG Graphics** - Vector illustrations and animations
- 📋 **Mermaid Diagrams** - Flowcharts and diagrams
- 💻 **Code Snippets** - Syntax-highlighted code

### **Key Features:**
- 🔍 **Auto-Detection** - Automatically detects artifact type from content patterns
- 📝 **Template System** - Pre-built templates for all artifact types
- 🎯 **Interactive Rendering** - Live preview with real-time updates
- 📊 **Performance Monitoring** - Render time and memory usage tracking
- 🛡️ **Secure Execution** - Sandboxed environment for safe code execution
- 📦 **CDN Integration** - Automatic library loading from trusted sources
- 💾 **Download Support** - Export artifacts as files
- 🔄 **Real-time Editing** - Live code editing with instant preview

### **New Artifact System Files:**
```
complexity/perplexity/extension/src/plugins/artifacts/
├── engine/
│   ├── ArtifactEngine.ts          # Core artifact orchestrator
│   ├── CDNManager.ts              # External library management
│   └── SecureSandbox.ts           # Safe code execution environment
├── renderers/
│   ├── P5Renderer.ts              # p5.js creative coding
│   ├── ThreeRenderer.ts           # Three.js 3D graphics
│   ├── D3Renderer.ts              # D3.js data visualization
│   ├── ReactRenderer.ts           # React component rendering
│   ├── HTMLRenderer.ts            # HTML page rendering
│   ├── SVGRenderer.ts             # SVG graphics rendering
│   ├── MermaidRenderer.ts         # Mermaid diagram rendering
│   └── CodeRenderer.ts            # Syntax highlighting
├── components/
│   ├── EnhancedArtifactCanvas.tsx # Full-featured artifact display
│   └── ArtifactIntegration.tsx    # Drop-in integration component
├── store/                         # State management
├── _locales/                      # Internationalization
└── artifacts-index.ts             # Export index
```

## Supported Platforms/Services

### Perplexity AI

  <div>
    <img src="https://img.shields.io/chrome-web-store/rating/ffppmilmeaekegkpckebkeahjgmhggpj?label=CWS%20rating" alt="Chrome Web Store Rating">
    <img src="https://img.shields.io/chrome-web-store/users/ffppmilmeaekegkpckebkeahjgmhggpj?label=CWS%20users" alt="Chrome Web Store Users">
    <img src="https://img.shields.io/amo/rating/complexity?label=AMO%20rating" alt="Mozilla Add-on Rating">
    <img src="https://img.shields.io/amo/users/complexity?label=AMO%20users" alt="Mozilla Add-on Users">
  </div>

- Provides a comprehensive set of added features and UI/UX improvements with excellent modularity and customization
- **NEW**: Complete artifact rendering system for creative coding and visualization
- Supports all available languages (22)
- Runs flawlessly on Firefox Android
- Available on:

  <a href="https://chromewebstore.google.com/detail/complexity/ffppmilmeaekegkpckebkeahjgmhggpj" target="_blank"><img src="./branding/cws.svg" width="200px"></a>
  <a href="https://addons.mozilla.org/en-US/firefox/addon/complexity/" target="_blank"><img src="./branding/amo.svg" width="200px"></a>

- Navigate to [`./perplexity/extension/`](./perplexity/extension/) for more information

## 📁 **Complete Project Structure**

```
complexity/
├── branding/                       # Branding assets and logos
│   ├── amo.svg
│   ├── cws.svg
│   ├── imgs/                       # Screenshots and images
│   ├── logo/                       # Logo variations
│   └── web-store/                  # Web store assets
├── packages/                       # Shared packages
│   ├── async-dep-manager/          # Async dependency management
│   ├── cli-logger/                 # CLI logging utilities
│   ├── eslint-config/              # ESLint configuration
│   ├── i18n/                       # Internationalization
│   └── typescript-config/          # TypeScript configuration
├── perplexity/                     # Perplexity AI extension
│   └── extension/                  # Main extension code
│       ├── changelogs/             # Version changelogs
│       ├── cli/                    # Command line tools
│       ├── docs/                   # Documentation
│       ├── e2e/                    # End-to-end tests
│       ├── eslint-config/          # Extension-specific ESLint config
│       ├── public/                 # Static assets
│       ├── src/                    # Source code
│       │   ├── _locales/           # Localization files
│       │   ├── assets/             # CSS and assets
│       │   ├── components/         # UI components
│       │   │   ├── ui/             # Base UI components
│       │   │   └── changelog/      # Changelog components
│       │   ├── data/               # Data management
│       │   │   ├── dashboard/      # Dashboard data
│       │   │   ├── plugin-registry/# Plugin registry
│       │   │   └── query-client/   # Query client setup
│       │   ├── entrypoints/        # Extension entry points
│       │   │   ├── background/     # Background scripts
│       │   │   ├── content-scripts/# Content scripts
│       │   │   └── options-page/   # Options page
│       │   ├── hooks/              # Custom React hooks
│       │   ├── plugins/            # Plugin system
│       │   │   ├── _api/           # Plugin API
│       │   │   ├── _core/          # Core plugins
│       │   │   ├── artifacts/      # 🆕 Artifact rendering system
│       │   │   │   ├── engine/     # Artifact engine
│       │   │   │   ├── renderers/  # Artifact renderers
│       │   │   │   ├── components/ # Artifact components
│       │   │   │   ├── store/      # State management
│       │   │   │   └── _locales/   # Localization
│       │   │   ├── better-search-params/
│       │   │   ├── better-sidebar/
│       │   │   ├── block-analytic-events/
│       │   │   ├── claude-code/    # Claude Code integration
│       │   │   ├── cloudflare-timeout-auto-reload/
│       │   │   ├── comet-isolated-zoom/
│       │   │   ├── command-menu/
│       │   │   ├── custom-thread-container-width/
│       │   │   ├── drag-n-drop-file-to-upload-in-thread/
│       │   │   ├── export-thread/
│       │   │   ├── force-writing-mode/
│       │   │   ├── hide-get-mobile-app-cta-btn/
│       │   │   ├── home-custom-slogan/
│       │   │   ├── image-gen-popover/
│       │   │   ├── incognito-by-default/
│       │   │   ├── language-model-selector/
│       │   │   ├── prompt-history/
│       │   │   ├── query-box-submit-on-ctrl-enter/
│       │   │   ├── slash-command/
│       │   │   ├── thread-better-code-blocks/
│       │   │   ├── thread-better-message-copy-buttons/
│       │   │   ├── thread-better-rewrite-dropdown/
│       │   │   ├── thread-message-length/
│       │   │   ├── thread-message-tts/
│       │   │   ├── thread-raw-headings/
│       │   │   ├── thread-toc/
│       │   │   └── zen-mode/
│       │   ├── services/           # Service layer
│       │   │   ├── cplx-api/       # API services
│       │   │   ├── extension-permissions/
│       │   │   ├── extension-settings/
│       │   │   ├── i18n/           # Internationalization
│       │   │   ├── indexed-db/     # Database services
│       │   │   ├── instant-css/    # CSS injection
│       │   │   ├── plugins-states/ # Plugin state management
│       │   │   └── pplx-api/       # Perplexity API
│       │   ├── types/              # TypeScript type definitions
│       │   ├── utils/              # Utility functions
│       │   └── vite-plugins/       # Vite build plugins
│       ├── tests/                  # Test files
│       ├── tsconfig.json           # TypeScript configuration
│       ├── vite.config.ts          # Vite build configuration
│       └── package.json            # Extension dependencies
├── pnpm-lock.yaml                  # Package lock file
├── package.json                    # Root package configuration
└── README.md                       # This file
```

## 🚀 **Getting Started**

### **For Users:**
1. Install the extension from [Chrome Web Store](https://chromewebstore.google.com/detail/complexity/ffppmilmeaekegkpckebkeahjgmhggpj) or [Firefox Add-ons](https://addons.mozilla.org/en-US/firefox/addon/complexity/)
2. Enable the **Artifacts** plugin in the extension settings
3. Start creating and rendering artifacts in Perplexity AI conversations

### **For Developers:**
1. Clone the repository: `git clone https://github.com/your-repo/complexity.git`
2. Install dependencies: `pnpm install`
3. Build the extension: `pnpm build`
4. Load the extension in your browser's developer mode

### **Artifact System Usage:**
```typescript
// Import the artifact system
import { ArtifactIntegration, detectArtifactType, createArtifact } from '@/plugins/artifacts';

// Auto-detect artifact type
const type = detectArtifactType(content, language);

// Create an artifact
const artifact = createArtifact(content, type, {
  title: 'My Creative Sketch',
  canvasSize: { width: 600, height: 400 }
});

// Use the integration component
<ArtifactIntegration 
  content={content}
  language="javascript"
  onUpdate={handleUpdate}
/>
```

## License

- [Full license terms](./LICENSE)
