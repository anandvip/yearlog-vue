# YearLog Vue.js Project Structure

## Initial Setup Commands
```bash
# Create new Vue.js project
npm create vue@latest yearlog-vue
cd yearlog-vue

# Select these options when prompted:
# ✅ TypeScript: No
# ✅ JSX: No  
# ✅ Router: Yes
# ✅ Pinia: Yes (for state management)
# ✅ Vitest: No
# ✅ E2E Testing: No
# ✅ ESLint: Yes
# ✅ Prettier: Yes

# Install additional dependencies
npm install
npm install @vueuse/core  # For PWA and utility composables
```

## Project Folder Structure
```
yearlog-vue/
├── public/
│   ├── manifest.json          # PWA manifest
│   ├── sw.js                  # Service worker
│   ├── ylg.png               # App icon
│   └── favicon.ico
├── src/
│   ├── assets/
│   │   └── styles/
│   │       └── global.css    # Global styles (converted from HTML)
│   ├── components/
│   │   ├── layout/
│   │   │   ├── AppHeader.vue     # Header with date, weekday, settings
│   │   │   ├── AppFooter.vue     # Footer with add button
│   │   │   └── RedLine.vue       # Vertical red line
│   │   ├── entries/
│   │   │   ├── EntryCard.vue     # Individual entry component
│   │   │   ├── EntryForm.vue     # Entry editing component
│   │   │   └── EntriesList.vue   # Entries container
│   │   ├── search/
│   │   │   ├── SearchPanel.vue   # Search panel with backdrop
│   │   │   ├── YearOverview.vue  # Year stats and month accordion
│   │   │   ├── RecentEntries.vue # Recent entries list
│   │   │   └── SearchResults.vue # Search results display
│   │   ├── ui/
│   │   │   ├── Modal.vue         # About modal
│   │   │   ├── Toast.vue         # Toast notifications
│   │   │   ├── ConfirmDialog.vue # Confirmation dialogs
│   │   │   └── SettingsPanel.vue # Settings dropdown
│   │   └── utils/
│   │       └── MarkdownRenderer.vue # Markdown parsing component
│   ├── composables/
│   │   ├── useEntries.js         # Entry management logic
│   │   ├── useSearch.js          # Search functionality
│   │   ├── useExport.js          # Export/import logic
│   │   ├── usePWA.js            # PWA installation logic
│   │   ├── useToast.js          # Toast notifications
│   │   ├── useMarkdown.js       # Markdown parsing
│   │   └── useDateInfo.js       # Date calculations
│   ├── stores/
│   │   ├── entries.js           # Entries state management
│   │   ├── ui.js               # UI state (modals, panels)
│   │   └── settings.js         # App settings
│   ├── utils/
│   │   ├── markdown.js         # Markdown parser utility
│   │   ├── export.js           # Export utilities
│   │   ├── storage.js          # Local storage utilities
│   │   └── date.js             # Date formatting utilities
│   ├── views/
│   │   └── HomeView.vue        # Main application view
│   ├── App.vue                 # Root component
│   ├── main.js                 # Application entry point
│   └── router/
│       └── index.js            # Router configuration
├── package.json
├── vite.config.js              # Vite configuration with PWA
└── README.md
```

## Key Dependencies to Add
```json
{
  "dependencies": {
    "@vueuse/core": "^10.x.x",
    "pinia": "^2.x.x", 
    "vue": "^3.x.x",
    "vue-router": "^4.x.x"
  },
  "devDependencies": {
    "vite-plugin-pwa": "^0.x.x"
  }
}
```

## Next Steps Breakdown
1. **Setup & Configuration** (package.json, vite.config.js, manifest.json)
2. **Global Styles** (Convert CSS to Vue-compatible format)
3. **Store Setup** (Pinia stores for state management)
4. **Utility Functions** (Date, markdown, storage helpers)
5. **Composables** (Reusable logic hooks)
6. **Base Components** (UI components like Modal, Toast)
7. **Layout Components** (Header, Footer, RedLine)
8. **Entry Components** (Entry management)
9. **Search Components** (Search functionality)
10. **Main Views** (App.vue, HomeView.vue)
11. **PWA Configuration** (Service worker, manifest)
12. **Build & Deploy Setup** (GitHub Pages configuration)

Should I proceed with Step 2 (Setup & Configuration files), or would you like me to wait until you're ready to continue?
