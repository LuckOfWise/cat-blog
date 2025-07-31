# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo-based cat blog called "ラムネの日々" (Ramune's Daily Life) featuring an office cat named ラムネ (Ramune). The site is deployed to GitHub Pages at https://luckofwise.github.io/cat-blog/.

## Architecture

- **Static Site Generator**: Hugo v0.148.2+ with the Ananke theme
- **Content**: Japanese-language blog posts about a cat named ラムネ (Ramune)
- **Theme**: Ananke theme located in `themes/ananke/`
- **Custom Layout**: Photo grid layout in `layouts/index.html` for Instagram-like photo display
- **Images**: Cat photos stored in `static/images/` and referenced in posts
- **Deployment**: GitHub Pages with `canonifyURLs = true` for proper asset handling

## Common Commands

### Development Server
```bash
hugo server -D
```
Starts local development server with draft content enabled.

### Build Site
```bash
hugo
```
Generates static site in `public/` directory for deployment.

### Theme Management
The Ananke theme is included as a git submodule in `themes/ananke/`. Theme customizations are made via:
- Custom `layouts/index.html` for photo grid display
- Configuration in `hugo.toml`

## Content Structure

### Blog Posts
- Location: `content/posts/`
- Format: Markdown with YAML frontmatter
- Naming: `post-YYYY-MM-DDTHH-MM-SS.md`
- Required frontmatter:
  ```yaml
  ---
  title: "Post title in Japanese"
  date: YYYY-MM-DD
  draft: false
  ---
  ```

### Images
- Location: `static/images/`
- Naming: `cat-YYYY-MM-DDTHH-MM-SS.jpg`
- Referenced in posts as: `![Alt text](/images/filename.jpg)`

## Site Configuration

Key settings in `hugo.toml`:
- `baseURL`: GitHub Pages URL
- `languageCode`: "ja-jp" (Japanese)
- `theme`: "ananke"
- `canonifyURLs`: true (required for GitHub Pages)
- `paginate`: 36 (photo grid pagination)
- `mainSections`: ["posts"]

## Custom Features

### Photo Grid Layout
The homepage (`layouts/index.html`) implements a responsive photo grid that:
- Extracts first image from each post's markdown
- Displays as Instagram-like grid with hover effects
- Responsive design with different column counts for various screen sizes
- Includes pagination for navigation

### Japanese Content
All content is in Japanese, including:
- Post titles and content
- Site title: "ラムネの日々"
- Hashtags in Japanese: #ラムネ #オフィス猫 #メヌエット

## Deployment

Site deploys automatically to GitHub Pages. The `public/` directory contains the generated static files and should not be manually edited.