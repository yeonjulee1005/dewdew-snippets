# Change Log

All notable changes to the "DewDew Snippets" extension will be documented in this file.

## [1.2511.1] - 2025-11-14

### Improved
- Enhanced Nuxt4 snippet formatting and structure
- Removed unnecessary `<script setup>` tags from Server Route, Middleware, and Plugin snippets
- Updated Component snippet: changed `emit` to `emits` and fixed event naming convention (`update-title` → `update:title`)
- Added `<slot />` to Layout snippet for proper slot usage
- Improved placeholder numbering and indentation across all Nuxt4 snippets
- Enhanced Server Route snippet with better example code
- Updated Middleware snippet parameters to use `_to, _from` convention for unused parameters
- Fixed JSON formatting and trailing commas for better code consistency

## [1.2509.1] - 2025-09-14

### Fixed
- Fixed minor version logic to properly handle YYMM format
- Updated version management scripts to correctly increment minor versions
- Improved version parsing for YYMM format compatibility

## [0.0.7] - 2025-08-18

### Fixed
- Reorganized snippet language mappings for better file type support
- .vue files now support both vue3 and nuxt4 snippets
- .jsx and .tsx files now support react, nextjs, and react-native snippets
- Improved snippet availability across different file contexts

## [0.0.6] - 2025-08-18

### Fixed
- Fixed Vue file snippet recognition by adding vue-html and javascript language support
- Improved snippet availability across different Vue file contexts
- Enhanced language identifier coverage for better snippet detection

## [0.0.5] - 2025-08-18

### Fixed
- Fixed publisher name to "DewdewSnippets" for consistency
- Updated SETUP.md documentation with correct publisher information
- Improved build process documentation

## [0.0.4] - 2025-08-18

### Fixed
- Fixed VS Code engine compatibility from ^1.102.0 to ^1.60.0 for Cursor compatibility
- Updated version to 0.0.4

## [0.0.3] - 2025-08-18

### Fixed
- Fixed publisher name from "DewdewSpinnets" to "DewdewSnippets"
- Fixed display name typo from "Develover" to "Developer"
- Updated language identifiers to match VS Code standards
- Fixed marketplace badge URL in README.md
- Added MIT License file

## [0.0.2] - 2025-01-27

### Added
- Vue3 Composition API Component
- Vue3 Pinia Store
- Vue3 Navigation
- Nuxt4 Page
- Nuxt4 Layout
- Nuxt4 Component
- Nuxt4 Composable
- Nuxt4 Server Route
- Nuxt4 Middleware
- Nuxt4 Plugin
- React Functional Component
- React Functional Component with Hooks
- React Custom Hook
- Zustand Local Store
- Zustand Global Store
- React Context
- React Event Handler
- Next.js App Router Page
- Next.js App Router Layout
- Next.js API Route
- Next.js Server Component
- Next.js Client Component
- Next.js Image Component
- Next.js Link Component
- Next.js Initial Props
- Next.js App
- Next.js Document
- Next.js API Handler
- Next.js Middleware
- React Native Functional Component
- React Native Screen Component

### Initial Release
- Documentation